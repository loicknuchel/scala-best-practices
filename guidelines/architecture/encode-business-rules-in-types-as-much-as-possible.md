# **[MUST] Encode business rules in types as much as possible**

types are  checked by the compiler, they can't be wrong, so if something is encoded in a type, it can't fail. Types are your first safety net, then comes the tests and last, the users...