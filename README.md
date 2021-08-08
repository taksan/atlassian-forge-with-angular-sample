# Atlassian forge sample app with angular

## Testing this application

This project is a sample atlassian forge app using Custom UI and and Angular for the front end

Steps to test this project:

1. Create a forge app using `forge create` just to get your application id (app > id)
2. Edit the manifest and fill the id with your generated id
3. Run:

```sh
forge deploy
forge install
```

## How to create your own

This application was mostly created using forge and ng regular commands. However, there are
couple of details to make it work properly with forge:

1. Make sure your manifest includes the following permissions:

    ```yaml
        permissions:
    content:
        styles:
        - 'unsafe-inline'
        scripts:
        - 'unsafe-eval'
    ```

2. Make sure your index.html base href is `<base href="">`
