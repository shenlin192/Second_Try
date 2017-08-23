# Dashboard 

## Usage

### development

1. Clone this repository
2. Install all the dependencies `npm install`
3. Start the application in localhost `npm start`

### deployment

1. Build for production `npm run build`
2. Copy and paste the built folder `build` to server under path `\static\dashboard`, and then rename `index.html` to `dashboard.html` 


## Architecture

Dashboard follows the Model–view–viewmodel (MVVM) architectural pattern. View layer is managed by React and the model layer is 
managed by Redux. Based on this MVVM architecture, a library called Antd is used. It provides a powerful Grid system and 
a large amount of rich feature build-in components. The role of `antd` in our `React-Redux` architecture is somehow similar as the role of
`bootstrap` in the classical usage of `HTML, CSS, JS, Jquery`.
 
### React Redux Architecture

The following image shows how Redux manage communication amount different React components.  

<img src="http://i.imgur.com/DUiL9yn.png" width="650">

Whenever information (state) in the store changes, components will be re-rendered automatically. 
If there is any user action that will make change to state, such action will be firstly dispatched to all the Reducers.
And then, these Reducers will match the action and make changes to the store accordingly. 
Once again, since the store is changed, corresponding components will get updated automatically.

### Antd

More info about Antd can be found [here](https://ant.design/docs/react/introduce).


### Component Tree
![](./Images/dashboard/dashboard_architecture_1 .png)
