# Some of the add ons used in react

### Font Awesome


Using Font awesome in react. 
Just change the name of icon in import to import different icon.

```
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
import { faCircle } from '@fortawesome/free-solid-svg-icons';
import { faPencilAlt } from '@fortawesome/free-solid-svg-icons';
```
### Redirecting in react

```
import { Redirect } from 'react-router';
\\ One way is to have a redirect state and make


### Getting Parameters from URL

[Reference](https://medium.com/better-programming/how-to-pass-multiple-route-parameters-in-a-react-url-path-4b919de0abbe) 


```
import queryString from 'query-string';

// Sending the parameters
Send Url like = url + '?userId=' + userId;

//Using the parameters
const { userId } = queryString.parse(this.props.location.search);
```

### Sending an email using React

[Reference](https://blog.mailtrap.io/react-send-email/) 

Just add. ( To change template, or fields, using dynamic variables like go to your emailjs account)

```
const templateId = 'template_8Ghi5MQi';
        this.sendEmail(templateId, {
          message_html:
            'http://localhost:3000/api/user/' +
            data.url +
            '?userId=' +
            this.state.userId,
          to: this.state.userId,
        });

sendEmail(templateId, variables) {
    window.emailjs
      .send('gmail', templateId, variables)
      .then((res) => {
        console.log('Email successfully sent!');
      })
      // Handle errors here however you like, or use a React error boundary
      .catch((err) =>
        console.error(
          'Oh well, you failed. Here some thoughts on the error that occured:',
          err
        )
      );
  }
```  
        