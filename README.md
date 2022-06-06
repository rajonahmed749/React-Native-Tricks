# React-Native-Tricks


## Android Safe Area View     
    
### [`Here is an example for Android Safe Area view `] 

    import { StyleSheet, View, SafeAreaView, Platform, StatusBar } from 'react-native'
    import React from 'react'

    export default function Home() {
        return (
            <SafeAreaView style={styles.AndroidSafeArea}>
                <View>                    
                    <Text>Here we enable safe area view in android devices</Text>
                </View>
            </SafeAreaView>
        )
    }

    // Create custom style
    const styles = StyleSheet.create({
        AndroidSafeArea: {
            flex: 1,
            paddingTop: Platform.OS === "android" ? StatusBar.currentHeight : 0
        }
    })
