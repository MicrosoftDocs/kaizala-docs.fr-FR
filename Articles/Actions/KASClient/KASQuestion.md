# <a name="kasquestion"></a><span data-ttu-id="4d6c7-101">KASQuestion</span><span class="sxs-lookup"><span data-stu-id="4d6c7-101">KASQuestion</span></span>
```typescript
class KASQuestion {
  // Index of the question, starts with 0
  public id: number;
  // Title of the question
  public title: string;
  // Type of the question
  public type: KASQuestionType;
  // Denotes if the question should be invisible to the responder, default is false
  public isInvisible: boolean;
  // Denotes if the question can be edited by the responder, default is true
  public isEditable: boolean;
  // List of options for the question
  public options: KASQuestionOption[];
}
```
