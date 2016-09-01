# LearnReactRedux-v-0.01

添加依赖

1.npm i react-native-material-design --save
2.npm install --save react-redux
3.npm install --save redux
4.npm install --save-dev redux-devtools
5.npm install react-native-vector-icons --save
    （1）android/app/build.gradle：
        project.ext.vectoricons = [
            iconFontNames: [ 'MaterialIcons.ttf', 'EvilIcons.ttf', 'Entypo.ttf', 'FontAwesome.ttf', 'Foundation.ttf', 'Ionicons.ttf', 'Octions.ttf', 'Zocial.ttf'] // Name of the font files you want to copy
        ]

        apply from: "../../node_modules/react-native-vector-icons/fonts.gradle"
    （2）android/settings.gradle： 
         include ':react-native-vector-icons'
         project(':react-native-vector-icons').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-vector-icons/android')
    （3）android/app/build.gradle：
        compile project(':react-native-vector-icons')
    （4）Edit your MainApplication.java：
        package com.myapp;

        + import com.oblador.vectoricons.VectorIconsPackage;

        ....

        @Override
        protected List<ReactPackage> getPackages() {
            return Arrays.<ReactPackage>asList(
            new MainReactPackage()
        +   , new VectorIconsPackage()
            );
        }

        }
