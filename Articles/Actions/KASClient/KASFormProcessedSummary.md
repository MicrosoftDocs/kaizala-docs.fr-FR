# <a name="kasformprocessedsummary"></a><span data-ttu-id="73bf0-101">KASFormProcessedSummary</span><span class="sxs-lookup"><span data-stu-id="73bf0-101">KASFormProcessedSummary</span></span>
```typescript
class KASFormProcessedSummary {
  // How many in the conversation did not respond
  public nonRespondersInConversation: number;
  // How many in the conversation were assigned to respond to this form
  public targetResponderCount: number;
  // How many total responses were received for the form, considering multiple responses from one person
  public totalResponseCount: number;

  // Aggregated result for aggregative questions
  // Dictionary<QuestionId: number, Result: KASQuestionResult>
  public results;
}
```
