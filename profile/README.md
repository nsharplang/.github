# The N# Language Group

Welcome to N# (sometimes called NSharp)! N# is an ongoing project that I work
on when I feel like it. Don't expect fast or consistent updates to this
project. This is the N# language "group" not because it's a group of people
developing it (it's not, it's just me), it's a language "group" because it
encompasses a variety of programming languages.

## What actually is N#?

N# is a group of programming languages used to achieve a universal goal. The N# languages are a mix of low and high levels of programming. Each language has a fairly easy-to-use syntax and can both be interpreted by the SDK or compiled to a variety of different formats, including executables and libraries for many processor types, a universal library format called "NSLib," and even to other N# language formats, going from high-level to low-level languages.

N# will also come with a variety of low and high level libraries for physics, math, graphics, and more. Focusing on the graphics library, a programmer will have a few choices for level of programming and capabilities. If the programmer chooses a high-level version of the library, graphics will be as easy as creating a camera, screen, and object and rendering the result. The result will be more CPU-intensive, but if someone wants to make something quick and dirty then this is the perfect option. On the other hand, if someone is a masochist and enjoys utilizing OpenGL to its fullest extent, that is an option as well, with the low-level library being nothing but a wrapper for direct access to GL.

## What are the N# languages?

Here they are:
| Name | Programming Level | Description |
|-|-|-|
| N# (NS) | High-Level | The main programming language in the group. Allows for easy programming of tricky topics. |
| N# Simplified (NSL) | High-Level | The benefits of the main language without all the syntax sugar and fluff. Used for writing more lightweight programs. |
| N# Intermediate Language (NIL) | Mid-Level | Allows for more direct access to the computer. |
| N# Assembly (NAS) | Low-Level | An easier to use and more universal form of assembly. Allows for nearly direct access to a processor. |

The languages will be able to compile to each other, following this pattern:

- N# can compile to N# Simplified, N# Intermediate, and N# Assembly
- N# Simplified can compile to N# Intermediate and N# Assembly, and decompile to N#.
- N# Intermediate can compile to N# Assembly and lossily decompile to N# and N# Simplified.
- N# Assembly cannot be decompiled and cannot compile into another language.

All languages can additionally compile to various OS and CPU executables and library formats and the universal NSLib format. All languages can import and utilize an NSLib file, though the ways they are used may change. N#, N# Simplified, and N# Intermediate will all access the library through very similar methods, however N# Assembly will require some more instructions to accomplish the same task.

## How is N# used?

N# programs are not compiled one file at a time. Instead, each program has its own project file, with XML-styled property info about what language is used, what the output will be, and other miscellaneous info. N# project files use the `.nsproj` extension and look a little something like this:

```xml
<Project>
    <Title>Example Project</Title>
    <Output>nslib</Output>
    <Language>nss</Language>
    <SdkVersion>1.0</SdkVersion>

    <OutputBinaryDirectory>./bin/</OutputBinaryDirectory>
    <OutputObjectDirectory>./obj/</OutputObjectDirectory>
</Project>
```

Once a project file is created, all files and folders inside the active directory are considered part of the project. Code files can reference each other as long as both are in the same root folder. Subdirectories are allowed. Exceptions include the directories specified for binary and object outputs in the project file.

The exact project file layout isn't known yet. Check out the docs when they exist for more info!

---

Thanks for checking this out! I just want to make it clear that I'm not going to finish this anytime soon. I'm just a solo guy and I'm by no means working on this 9-5. I work on it whatever days I feel like it for however long I feel like it. So don't expect me to be consistent. It'll likely be years before anything super meaningful happens here. Don't get hyped up.
