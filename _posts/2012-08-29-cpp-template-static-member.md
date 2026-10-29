---
title: A template static member that GCC won't link
subtitle: C++ hell
description: "GCC won't link a declared explicit specialisation of a template's static data member until it has an initialiser, and the standard agrees."
date: 2012-08-29 12:12
tags: [cpp]
---
Nobody can know all of C++. The following code fails to link with GCC, complaining about an undefined variable:

```cpp
template <typename T>
struct core_type
{
public:
	static int m_var;
};

struct test_type : public core_type<test_type>
{
	int m_another_var;
};

template<> int core_type<test_type>::m_var;
```

If I change the last line to this, it compiles successfully:

```cpp
template<> int core_type<test_type>::m_var = 0;
```

And that is the correct behaviour. *ISO/IEC 14882 (14.7.3.15) says that an explicit specialization of a static data member of a template is a definition only when it includes an initializer. There is no syntax to define it with default value.*

Visual Studio accepts the first version without any error.
