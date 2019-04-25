# <a name="kasoptionresult"></a><span data-ttu-id="7e0c3-101">KASOptionResult</span><span class="sxs-lookup"><span data-stu-id="7e0c3-101">KASOptionResult</span></span>
```typescript
class KASOptionResult {
  // Title of the option
  public optionTitle: string;
  // Index of the option
  public optionId: number;
  // How many have chosen this option
  public totalResponsesCount: number;
  // A map of user ids against their response count
  // Dictionary<UserId: string, ResponseCount: number>
  public responderToResponseCount;
}
```

