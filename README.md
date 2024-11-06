### Mangebuilder App Project Overview
I have developed an Angular (2+) CRUD application for managing people. The application allows users to create, list, display details, edit, and delete individuals. Each person is characterized by attributes such as ID, first name, last name, and email address.

For the backend service, I implemented a mock/fake version. Although it doesn't interact with a real backend, the requests and responses are provided in JSON format to simulate the expected behavior.

Throughout the development process, I followed a Test-Driven Development (TDD) approach. This involved writing tests before implementing each feature and ensuring they passed successfully. By adhering to TDD principles, I aimed to create a reliable and maintainable codebase.

I documented my development steps, providing detailed explanations for the decisions I made along the way. This documentation serves as a reference for future maintenance and improvement of the application.

Regarding the user interface, I kept it simple and focused on functionality. A basic list is used to display the people, and there is no need for styling, filtering, or sorting in this version of the application. The primary emphasis was on implementing the CRUD operations effectively and ensuring a smooth user experience.
The Mangebuilder app is a small-scale Angular application designed for managing personnel data with specific core functionalities, including creating, reading, updating, and deleting (CRUD) personnel records. Each person has unique attributes: an ID (non-editable), first name, last name, and email address. This app enables users to:

1. **Create new personnel records**  
2. **List all personnel by name**  
3. **View detailed information about each individual**  
4. **Edit personnel information**  
5. **Remove individuals from the list**

### Project Objective
The primary goal of this project is to develop a streamlined Angular application that allows basic personnel management functionalities in a user-friendly and efficient interface. Using a mock backend server, it provides a simulation of real data interactions without requiring an actual backend infrastructure.

### Tools and Tech Stack
The project utilizes the following tools and technologies:
- **UI Framework:** Angular
- **Mock Backend:** JSON Server (for data storage and retrieval)
- **CSS and Styling:** Bootstrap (for responsive design and easy-to-use styling components)

### Development Steps

1. **Service Creation**  
   The project begins with creating a service to handle HTTP requests, using Angular's `HttpClient` module from `@angular/common/http`. This service acts as an intermediary between the JSON server and the Angular components, ensuring that all CRUD operations are properly executed.

2. **Implementation of CRUD Logic**  
   Since the application has straightforward logic with minimal components, it was designed without dedicated Angular components specifically for each CRUD operation. Instead, all CRUD logic is embedded within `application.component.ts`. This approach optimizes the structure for simplicity and maintains all operations in a single place, aligning with the project's small-scale scope.

3. **UI Design and Form Handling**  
   In the HTML templates, Bootstrap-based reactive forms are used to handle input values for creating and updating personnel records. Bootstrap tables are also utilized to display the list of personnel records effectively. Angular’s in-built directives (e.g., `*ngFor` for loops and event handling) allow for streamlined conditional logic, event emitters, and efficient rendering of lists within the HTML templates.

   ```html
   <tr *ngFor="let row of person">
      <td> {{row.id}} </td>
      <td> {{row.FirstName}} </td>
      <td> {{row.LastName}} </td>
      <td> {{row.age}} </td>
      <td>
         <button (click)="CreatePerson()" type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModalCenter">
         Add
         </button>
      </td>
   </tr>
   ```

### Technical Notes
- **JSON Server Setup**  
  The JSON Server is used to create a mock backend for testing and demonstration purposes. It can be installed globally with the following command:

   ```bash
   npm install -g json-server
   ```

   To start the server, use:
   ```bash
   json-server --watch db.json
   ```

   This server will be accessible at `http://localhost:3000`, acting as the backend endpoint for all CRUD operations.

- **Bootstrap Integration**  
  For styling, Bootstrap was added directly to the project by linking to its CDN in `index.html`. The integration can be completed by adding the following lines:

   ```html
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"
           integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN" crossorigin="anonymous"></script>
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet"
         integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">
   ```






# ManageBuilder

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.0.4.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
