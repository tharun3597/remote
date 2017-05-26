
React-Native-Login
	A React native login form component using Redux-Forms.

Example
 
 
 
 
Usage
 
import {
  StyleSheet,
  Text,
  View,
  TextInput
} from "react-native";
import React, { Component } from "react";

export default class Form extends React.Component {
  constructor(props) {
    super(props);
  }
  handleSubmit = (values, resolve, reject) => {
    //handlesubmit function
    //on_success and on_failure functions 
    resolve();
  };

  render() {
    return (
      <View style={styles.container}>
        <Login
          handlesubmit={this.handleSubmit}
          form="testing"
          style="loginform"
          fields={[
            {
              className: "fieldstyle",
              label: "Username",
              name: "username",
              placeholder: "Username",
              input_type: "text",
              regex: "optional",
              required: true,
              error_message: "Required",
              default_value: ""
            },
            {
              className: "fieldstyle",
              label: "Password",
              name: "password",
              placeholder: "Password",
              input_type: "password",
              regex: "optional",
              required: true,
              error_message: "Required",
              default_value: ""
            },
            {
              className: "fieldstyle",
              label: "Email",
              name: "email",
              placeholder: "email",
              input_type: "email",
              required: false,
              error_message: "Invalid email address",
              default_value: ""
            },
            {
              className: "fieldstyle",
              label: "Mobile Number",
              name: "mobile",
              placeholder: "Mobile Number",
              input_type: "mobile number",
              regex: "optional",
              required: true,
              error_message: "Required",
              default_value: ""
            }
          ]}
        />
      </View>
    );
  }
}
const styles = StyleSheet.create({
  view: {
    flex: 1
  },
  container: {
   flex: 1,
  },
  fieldstyle: {
   //styles for the field
  }
});
