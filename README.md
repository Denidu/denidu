import React, { Component } from 'react';

class Denidu extends Component {
  constructor() {
    super();
    this.state = {
      variables: {
        name: 'Denidu Gamage',
        age: 23,
      },
      platforms: {
        LinkedIn: 'www.linkedin.com/in/denidu',
        Instagram: '_deniiiduu_',
      },
    };
  }

  description() {
    return (
      <div>
        <h1>👋 Hi there, I'm Denidu Gamage!</h1>
        <p>
          I'm a passionate software developer with a love for coding and building cool things. Currently 23 years old and always eager to learn new technologies.
        </p>
        <ul>
          <li>Name: {this.state.variables.name}</li>
          <li>Age: {this.state.variables.age}</li>
        </ul>
      </div>
    );
  }

  socialMedias() {
    return (
      <div>
        <h2>🌐 Connect with me</h2>
        <ul>
          <li>
            LinkedIn: <a href="https://www.linkedin.com/in/denidu"  target="_blank" rel="noopener noreferrer">{this.state.platforms.LinkedIn}</a>
          </li>
          <li>
            Instagram: <a href="https://www.instagram.com/_deniiiduu_"  target="_blank" rel="noopener noreferrer">{this.state.platforms.Instagram}</a>
          </li>
        </ul>
      </div>
    );
  }

  render() {
    return (
      <div>
        {this.description()}
        {this.socialMedias()}
      </div>
    );
  }
}

export default Denidu;
