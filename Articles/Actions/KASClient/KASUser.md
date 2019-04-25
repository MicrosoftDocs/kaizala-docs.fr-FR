# <a name="kasuser"></a><span data-ttu-id="8efac-101">KASUser</span><span class="sxs-lookup"><span data-stu-id="8efac-101">KASUser</span></span>
```typescript
class KASUser {
  // Unique user id
  public id: string;
  // Name of the user ("You" for the current user)
  public name: string;
  // Not considering "You"
  public originalName: string;

  // Profile picture url of the user
  public pictureUrl: string;
  // Phone number of the user
  public phoneNumber: string;
  // In case the PictureUrl is not there, we should use the users initials as the profile pic, below two members are for that
  public pictureBGColor: string;
  public pictureInitials: string;
}
```
