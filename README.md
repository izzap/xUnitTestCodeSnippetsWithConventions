# xUnit Test Code Snippets


## Summary

This is "code snippets" for Microsoft Visual Studio 2012 or higher.

Is based on [jsakamoto](https://github.com/jsakamoto/xUnitTestCodeSnippets) xUnintTestCodeSnippets project. Adding naming convention to test methods and arrange, act, assert test body

## How to install

## How to use

### Insert xUnit Fact

On C# source code in Visual Studio, you can insert **xUnit Fact method** by following key typing.

- `xtestm` [Tab]  
or
- `fact` [Tab]

Then, this snippet expanded following C# code.

```csharp
[Fact]
public void MethodName_StateUnderTest_ExpectedBehavior()
{
    //arrange
    throw new NotImplementedException();

    //act

    //assert
}
```

#### with Display Name

- `dfact` [Tab]

```csharp
[Fact(DisplayName = "")]
public void MethodName_StateUnderTest_ExpectedBehavior()
{
    //arrange
    throw new NotImplementedException();

    //act

    //assert
}
```

### Insert xUnit Theory

And you can also insert **xUnit Theory method**.  
if you type following keys,

- `theory` [Tab]

Then, this snippet expanded following C# code.

```csharp
[Theory]
public void MyTheory()
{
    //arrange
    throw new NotImplementedException();

    //act

    //assert
}
```

#### with Display Name

- `dtheory` [Tab]

```csharp
[Theory(DisplayName = "")]
public void MyTheory()
{
    throw new NotImplementedException();
}
```

### Insert xUnit Test Class

And you can also insert **xUnit test class**.  
if you type following keys,

- `xtestc` [Tab]

Then, this snippet expanded following C# code.

```csharp
public class MyTestClass
{
    [Fact]
    public void MyTestFact()
    {
        throw new NotImplementedException();
    }
}
```

## and, "async" versions

- `afact`

```csharp
[Fact]
public async Task MyTestFact()
{
    throw new NotImplementedException();
}
```

- `dafact`

```csharp
[Fact(DisplayName = "")]
public async Task MyTestFact()
{
    throw new NotImplementedException();
}
```

- `atheory`

```csharp
[Theory]
public async Task MyTheory()
{
    throw new NotImplementedException();
}
```

- `datheory`

```csharp
[Theory(DisplayName = "")]
public async Task MyTheory()
{
    throw new NotImplementedException();
}
```

## Release Note

- v.1.5.0
  - Throw NotImplementedException by default.
- v.1.4.1
  - Fix: Cannot install on latest VS 2019 (16.1)
- v.1.4.0
  - Add suuport for Visual Studio 2019.
  - Snippets with "DisplayName" are added (`dfact`, `dafact`, `dtheory`, `datheory`).
- v.1.3.0
  - Add `afact` and `atheory` snippets to insert "async Task ..." methods.
- v.1.2.0
  - Add `theory` and `xtestc` snippets.
- v.1.1.0
  - Add `fact` snippet.
- v.1.0.0
  - 1st release, it contains `xtestm` snippet.


## License

[GNU GPL v.3](LICENSE.txt)
