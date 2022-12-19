import React from "react";
import { ImageBackground, StyleSheet, View } from "react-native";

import AppButton from "../components/AppButton";

export default function WelcomeScreen({ navigation }) {
  return (
    <ImageBackground
      style={styles.background}
      source={require("../assets/IMG_0283.JPG")}>
      <View style={styles.logoContainer}>
      </View>
      <View style={styles.ButtonView}></View>
      <AppButton title="Login" onPress={() => navigation.navigate('LoginScreen')} />
      <AppButton title="Register" color="secondary" onPress={() => navigation.navigate('RegistrationScreen')} />
    </ImageBackground>
  );
}
const styles = StyleSheet.create({
  background: {
    flex: 1,
    justifyContent: "flex-end",
    alignItems: "center",
    width: "100%"
  },
  logo: {
    width: 100,
    height: 100,
  },
  logoContainer: {
    position: "absolute",
    top: 70,
    alignItems: "center",
  },
  ButtonView: {
    width: "100%",
    paddingTop: 20,
  },
  TextSay: {
    fontSize: 26,
    fontWeight: "600",
    paddingVertical: 20,
  }
});