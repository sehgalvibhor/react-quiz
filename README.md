# reactjs-quiz [![npm version](https://badge.fury.io/js/reactjs-quiz.svg)](https://badge.fury.io/js/reactjs-quiz) [![License](https://img.shields.io/npm/l/react-quiz-component.svg)](https://github.com/wingkwong/react-quiz-component/blob/master/LICENSE) [![Total NPM Download](https://img.shields.io/npm/dt/reactjs-quiz.svg)](https://www.npmjs.com/package/reactjs-quiz)

reactjs-quiz is a React component used for creating quizzes, It's built on top of code by Wong, Wing Kam, just customized as per my needs and probably yours too.

## Installing
```
npm i reactjs-quiz
```

## Importing react-quiz-component
```
import Quiz from 'reactjs-quiz';
```

## Defining Your Quiz Source
The quiz source is a JSON object.
```javascript
export const quiz =  {
  "quizTitle": "React Quiz Component Demo",
  "quizSynopsis": "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim",
  "questions": [
    {
      "question": "How can you access the state of a component from inside of a member function?",
      "questionType": "text",
      "answers": [
        "this.getState()",
        "this.prototype.stateValue",
        "this.state",
        "this.values"
      ],
      "correctAnswer": "3",
      "messageForCorrectAnswer": "Correct answer. Good job.",
      "messageForIncorrectAnswer": "Incorrect answer. Please try again.",
      "explanation": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    },
    {
      "question": "ReactJS is developed by _____?",
      "questionType": "text",
      "answers": [
        "Google Engineers",
        "Facebook Engineers"
      ],
      "correctAnswer": "2",
      "messageForCorrectAnswer": "Correct answer. Good job.",
      "messageForIncorrectAnswer": "Incorrect answer. Please try again.",
      "explanation": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    },
    {
      "question": "ReactJS is an MVC based framework?",
      "questionType": "text",
      "answers": [
        "True",
        "False"
      ],
      "correctAnswer": "2",
      "messageForCorrectAnswer": "Correct answer. Good job.",
      "messageForIncorrectAnswer": "Incorrect answer. Please try again.",
      "explanation": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    },
    {
      "question": "Which of the following concepts is/are key to ReactJS?",
      "questionType": "text",
      "answers": [
        "Component-oriented design",
        "Event delegation model",
        "Both of the above",
      ],
      "correctAnswer": "3",
      "messageForCorrectAnswer": "Correct answer. Good job.",
      "messageForIncorrectAnswer": "Incorrect answer. Please try again.",
      "explanation": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    },
    {
      "question": "Lorem ipsum dolor sit amet, consectetur adipiscing elit,",
      "questionType": "photo",
      "answers": [
        "https://dummyimage.com/600x400/000/fff&text=A",
        "https://dummyimage.com/600x400/000/fff&text=B",
        "https://dummyimage.com/600x400/000/fff&text=C",
        "https://dummyimage.com/600x400/000/fff&text=D"
      ],
      "correctAnswer": "1",
      "messageForCorrectAnswer": "Correct answer. Good job.",
      "messageForIncorrectAnswer": "Incorrect answer. Please try again.",
      "explanation": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    }
  ]
} 
```

## Passing to Quiz container
```javascript
 import { quiz } from './quiz';
 ...
 <Quiz quiz={quiz}/>
```

## Shuffling question set
```javascript
 import { quiz } from './quiz';
 ...
 <Quiz quiz={quiz} shuffle={true}/>
```


## onComplete Callback
Returns number of correct responses
```javascript
 import { quiz } from './quiz';
 ...
 <Quiz quiz={quiz} shuffle={true} onComplete={(result) => console.log(result)}/>
```


## Props

|Name|Type|Default|Required|Description|
|:--|:--:|:-----:|:--|:----------|
|quiz|`object`|`null`|Y|Quiz Json Object|
|shuffle|`boolean`|`false`|N|Shuffle the questions|
|onComplete|`function`|`null`|N|Add a Callback|

## Development
- Clone the project
- run `npm install`
- run `npm run dev`

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
