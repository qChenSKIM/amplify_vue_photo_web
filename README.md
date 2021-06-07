## Steps:
### Install packages
1. npm install -g @vue/cli
2. vue --version
-   [problem](https://dewcodes.com/tutorials/solution-vue-cli-error-in-vs-code-vue-ps1-cannot-be-loaded/)
3. npm install -g @aws-amplify/cli
4. amplify
5. clear
### crete vue project
1. vue create photobook-yt
2. cd photobook-yt
3. npm run serve
### configure amplify/vue
1. vue add tailwind
2. npm install uuid
3. amplify configure
4. amplify init
   - [amplify init](./assets/1.png)
5. npm install aws-amplify @aws-amplify/ui-vue
 
changing src/main.js ==> importing Amplify

### amplify auth
1. amplify status
2. amplify add auth
3. amplify push
4. write login/logout code, add auth parts 

### amplify storage, api
1. amplify add storage
   - [amplify add storage](./assets/2.png)
2. amplify add api
   - [amplify add api](./assets/3.png)
3. open GraphAPI in localhost port (or you can login AWS AppSync)
    - amplify mock api
    - [amplify add api](./assets/4.png)
    - [amplify add api](./assets/5.png)
    - [amplify add api](./assets/6.png)
4. amplify push 
5. write code

### amplify function
1. amplify add function
   - [amplify add api](./assets/7.png)
2. cd amplify/backend/function/AmplifyPhotoProcessor/src
3. npm install axios aws4 exif-reader
4. npm install --arch=x64 --platform=linux sharp
5. write code
   
#### set s3 as lambda trigger
1. amplify storage update
   - [amplify add api](./assets/7.png)
2. change 'amplify/backend/function/AmplifyPhotoProcessor/AmplifyPhotoProcessor-cloudformation-template.json'- add 'MemorySize: 1536'
3. amplify push

## Result:
[result](./assets/amplify_vue_photo.gif)
