## Extension methods

### General guidance
- [Put extension methods in their own namespaces](own-namespace.md) 
- [Prefer to extend an interface over a class](extend-interface-over-class.md)

### When to use extension methods
- [For very general operations](only-for-general-operations.md)
- [To promote SRP](promote-srp.md)
- [To hide advanced functionality](hide-advanced.md)
- [When you don't have control of the code you wish to extend](no-control.md)
- [To avoid heavy breaking changes](breaking-changes.md)

### When not to use extension methods

When your use case does not fall in to one of the above. Create a method on the interface / class itself.