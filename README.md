
# Hollow Knight Modpack Sources

Hollow Knight Modpack Sources is a repository for **hpackages**.
You can post the modpacks you make here. But if you want to publish mods, please go to [hk-modlinks](https://github.com/hk-modding/modlinks)

## How to add/update a modpack to Modpack Sources

1. create a fork
2. add/update modpack json
3. create pull request
4. Github Action check passed and automatically merged after waiting for half an hour

### Requirements

**The following conditions must be met to be automatically merged**

1. The added/modified files cannot be located in the root directory
2. The name of the added/modified file and the names of all its parent folders cannot start with `.`
3. Only allow adding/modifying json files
4. The added/modified json format conforms to the following schema.
   - [hpackage](https://github.com/hpackage/hpackage-schema/tree/main)
   - [hkmmpackV1](https://github.com/hkmodmanager/hkmm-schema/blob/main/hkmm-schema/hkmmpackage.v1.schema.json)

## How to write modpack

Refer to [hpackage](https://github.com/hpackage/hpackage-schema/tree/main) and [hkmmpackV1](https://github.com/hkmodmanager/hkmm-schema/blob/main/hkmm-schema/hkmmpackage.v1.schema.json)

### Additional requirements

1. Required field: `name`, `description`, `version`, `authors`
2. At least one item in `authors` has the same name as the parent folder. 
   - For example, if the file location is `Folder 1/Folder 2/Folder 3/Modpack.json`, then at least one item in the `authors` field is `Folder 1` (case sensitive)

### Example 
- [Test 1](https://github.com/hkmodmanager/ModpackSource/blob/main/Test/Test1.json)
- [Test 2](https://github.com/hkmodmanager/ModpackSource/blob/main/Test/Test2/Test2.json)
