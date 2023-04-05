NO1
The event loop is a crucial component of the JavaScript language, responsible for managing asynchronous operations and ensuring that the code executes in a non-blocking way.In essence, the event loop continuously monitors the JavaScript runtime environment for events or tasks to execute, such as user input or network requests. These events are then added to a queue, which is processed one task at a time, in the order they were added. When a task is executed, the event loop will check if the task is synchronous or asynchronous. If the task is synchronous, it will execute immediately and the event loop will move on to the next task in the queue. If the task is asynchronous, it will be moved to a separate thread for execution, and the event loop will continue to process other tasks in the queue.Once the asynchronous task is completed, its result is placed in a callback queue, which is also monitored by the event loop. If there are any callbacks waiting in the queue, the event loop will execute them one at a time, in the order they were added.Overall, the event loop is responsible for managing the execution of tasks in a way that is both efficient and non-blocking, ensuring that the JavaScript code remains responsive and performant even when dealing with complex and time-consuming operations.                                                                                                                                                   
NO2                                                                                                                                               
Timers: In this phase, the event loop checks for any scheduled timer tasks that have reached their designated timeout value. If any such tasks are found, they are moved to the task queue for execution in the next phase.
Pending, Idle, prepare: This phase is rarely used in practice, and is mainly reserved for internal use by the Node.js runtime.
Poll: In this phase, the event loop waits for new I/O events or timer tasks to be added to the task queue. If any such events or tasks are found, they are processed immediately. If not, the event loop will wait until new events or tasks are added.                                                           
Check: In this phase, the event loop executes any callbacks that were added to the task queue during the previous phases. This phase is typically used for handling callbacks related to the completion of I/O events spefically where any setImmediate timers as part of the input/output are executed
Close callbacks: In this final phase, the event loop executes any remaining close callbacks related to the closing of network connections or other resources.

NO3
Use of asynchronous programming: Node.js is designed to work with asynchronous programming, so it's important to make use of asynchronous functions and callbacks to prevent blocking the event loop. Use of Promises and async/await are important tools in modern JavaScript development that allow to write asynchronous code that looks like synchronous code. They can help simplify complex logic and make code more readable.

Proper error handling: To always handle errors properly and gracefully. Using of the try-catch blocks or error-first callbacks, and to ensure that the errors are logged for debugging purposes.

Use of modules and packages: Node.js has a rich ecosystem of modules and packages that can be used to simplify code development. It is important to note that it is best to always use popular and well-maintained packages that have been tested and verified by the community.

Keepind code modular: Breaking up our code into smaller, reusable modules that can be tested and maintained easily. This makes code easier to read, understand, and debug.

Use a linter: Use a linter like ESLint to ensure that your code follows best practices, is consistent, and free of syntax errors. Linters can help catch errors and improve code quality.

Use of Prettier: Prettier is also a best practice for server-side code development in Node.js. Prettier is a code formatter that helps enforce consistent code style and makes code more readable. By using Prettier, you can ensure that your code adheres to a set of agreed-upon style guidelines and that formatting is consistent across your codebase. Prettier can be integrated with your text editor or integrated development environment (IDE) and can be set up to automatically format your code as you write it. This can help save time and ensure that code is consistently formatted, making it easier to read and understand.

Good naming conventions can help make code more readable and easier to understand, while comments can provide context and explain complex code logic. Similarly, well-defined functions can make code more modular and easier to test, as well as easier to understand and modify.

NO4 AND 5
npm5 is a version of the npm (Node Package Manager) tool for managing packages in Node.js applications. It can be initialized via command line using "npm init -y" and then this creates a package.json which contains metadata of the package

N06
To run a script defined in the package.json file of your Node.js project, you can use the npm run command followed by the script name.

