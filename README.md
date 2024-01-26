### Hi there 👋

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
        Email: 'denidugamage21@gmail.com',
      },
    };
  }

  description() {
    console.log('---deniduu---');
    Object.values(this.state.variables).forEach((value, index) => {
      switch (index) {
        case 0:
          console.log(`Name: ${value}`);
          break;
        case 1:
          console.log(`Age: ${value}`);
          break;
        default:
          break;
      }
    });
  }

  socialMedias() {
    console.log('\n-----contact-----');
    Object.entries(this.state.platforms).forEach(([key, value]) => {
      console.log(`${key}: ${value}`);
    });
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

export default denidu;
