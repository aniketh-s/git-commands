### Settings

- Name
- Email
- Default Editor
- Line ending

### Configuration Levels

- System
- Global
- Local

**Spcifying Levels**: 
```bash
git config --global user.name="name" #Within double quotes cause of space b/w names
git config --global user.email=email
```

### End of Lines:

![[Git Settings-20250528115132438.png]]

To prevent end of line issues in git, we configure the end of line properly with ```core.autocrlf ``` which stands for **carriage return line feed**

*Carriage Return Line Feed. It's a combination of two control characters used to indicate the end of a line in text and protocols, especially in HTTP.*

![[Git Settings-20250528115611163.png]]


By using core.autocrlf git adds/modifies end of line only when storing any code in the repo.
Setting for **Windows: true**
Setting for **Mac: input**
