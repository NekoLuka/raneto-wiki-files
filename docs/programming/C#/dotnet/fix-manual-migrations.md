## How to fix it when people manually edit configurations

Create a migration that has all the missing things.
```
dotnet ef migrations add DeleteMe
```

After this, manually delete this migration.
This is so that `ApplicationDbContextModelSnapshot.cs` is aware of the changes and won't propose them again.
Now create your real migration and run it against the database.
