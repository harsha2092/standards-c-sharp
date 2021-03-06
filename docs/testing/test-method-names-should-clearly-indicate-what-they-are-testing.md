## Test method names should clearly indicate what they are testing

- A test's purpose (its pre- and post-conditions) should be obvious from its name alone. It should not be necessary to read the code to work out what is being tested.
- A broken test is much easier to fix when it is obvious what is being tested and therefore what must have broken.
- This is strongly related to [tests as a specification](tests-as-a-specification.md).

Therefore, names tests in one of the following formats:

```c#
public class <SystemUnderTest>Tests 
{
    // seperated by underscores
    [Test]
    public void <SubsystemUnderTest>_<PostCondition>()
    {...}

    // or
    [Test]
    public void <SubsystemUnderTest>_<PreCondition>_<PostCondition>()
    {...}
}
```

For a unit test, the `<SystemUnderTest>` should be the class name, and the `<SubsystemUnderTest>` should be the method name.

### Don't

```c#
[Test]
public void HazardLightsTest()
{...}
```

### Do

```c#
[Test]
public void HarzardLightsToggle_WhenLightsAlreadyBlinking_BlinkingShouldStop()
{...}
```

If you are having difficutly naming your test this way, it might indicate it is doing too much and should be split into more [granular tests](tests-should-be-short-and-simple.md).