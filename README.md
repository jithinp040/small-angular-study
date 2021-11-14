# Angular Study Note:

## Install Angular and Create a new Project :
```bash
npm install -g @angular/cli 
```
  - And check installation by typing:
  ```bash
  ng --version
  ```
  - The above command should show you the version along with the dependenices of the Angular cli

### Create a new App:
```bash
ng new "app-name"
```
### To run the Server:
```bash
ng serve hostname
```
- *note:* The angular app runs on port *4200* by default.

### To create a component:
```bash
ng g c "component-name"
```
  - where:
    - g - generate
    - c - component
This creates a folder in the *src/app* directory with the component name as folder name with four files.
  - .ts - typescript 
  - spec.ts - test cases
  - .scss/css - styles
  - .html - view
The good thing about this is, this format encourages MVC architecture.

#### To use a component:
- Fill up the html & css details.
- Go to the *component-name.ts* file.
- Under the *@component* function, there will be a attribute named *selector*. Change the name of your selector as per your wish.
  - The other properties inside this are, templateUrl & stylesheetUrl   
- Write the selector value as tag to use it as a component anywhere.

#### Perform request inside component:
- To make *GET* and *POST* requests we require *HttpClient* module under the **`@angular/common/http`**
  - Use this *HttpClent* inside the *constructor* using format 
  ```ts
  private variablename : Module
  ```
- The important thing to note regarding requests in angular is that. Angular follows the **Observable model**. A request is sent and the result is received by **subscribing** to the event.

#### Working in html file:
- We can use the *\*ngIf* keyword to specify a condition to be followed for a component to be rendered inside the html file. The syntax is as follows:
```html
<tagname *ngIf="con dition"></tagname>
```
- We can utilize a variable of *ts* file as content by using this syntax **{{variableName}}**
- We can perform looping of a array by using the *\*ngFor* keyword. The syntax is as follows:
```html
<tagname *ngFor="let element of array">
  <tagname>Content</tagname>
</tagname>
```
- To utilize a variable of ts in the html as input we need to use *#variableName*

### Events:
- **Angular** -- **React**
- **ngInit** -- **componentDidMount**

## Notes:
- Each html file will have *router-outlet* tag at the bottom.
- Each variable inside the ts file is accessed using **this** keyword. (Similar to react class component)
