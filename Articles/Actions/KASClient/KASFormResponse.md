# <a name="kasformresponse"></a><span data-ttu-id="88ba2-101">KASFormResponse</span><span class="sxs-lookup"><span data-stu-id="88ba2-101">KASFormResponse</span></span>
```typescript
class KASFormResponse {
  // A unique response id, required in case of updating an existing response
  public id: string;
  // A map for serverUrl against localUrl of all the image attachments to a response
  // Dictionary<ServerUrl: string, LocalUrl: string>
  public serverToLocalAssetUrlMap;
  // A map of question id to answer
  // Dictionary<QuestionId: number, Answer: string>
  public questionToAnswerMap;
}
```