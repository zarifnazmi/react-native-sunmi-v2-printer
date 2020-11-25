
# react-native-sunmi-v2-printer

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/suraneti/react-native-sunmi-inner-printer/master/LICENSE) [![npm version](https://badge.fury.io/js/react-native-sunmi-v2-printer.svg)](https://www.npmjs.com/package/react-native-sunmi-v2-printer)

## SUNMI V2 Printer for React-Native

### Caution: this is not the official project and forked form https://github.com/januslo/react-native-sunmi-inner-printer

Offical Demos refer: https://github.com/shangmisunmi/SunmiPrinterDemo

## Installation

**Step 1.**

Install via NPM

```bash
npm install react-native-sunmi-v2-printer --save
```

Install via Yarn

```bash
yarn add react-native-sunmi-v2-printer
```

Install from source

```bash
npm install https://github.com/suraneti/react-native-sunmi-v2-printer.git --save
yarn add https://github.com/suraneti/react-native-sunmi-v2-printer.git --save
```

**Step 2:** (For React-Native < 0.60)

Links this plugin to your project.

```bash
react-native link react-native-sunmi-v2-printer
```

or you may need to link manually

* modify settings.gradle

```javascript
include ':react-native-sunmi-v2-printer'
project(':react-native-sunmi-v2-printer').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-sunmi-v2-printer/android')
```

* modify  app/build.gradle,add dependenceie：

```javascript
compile project(':react-native-sunmi-v2-printer')
```

* adds package references to  MainPackage.java

```java
import com.sunmi.innerprinter.SunmiInnerPrinterPackage;
...

 @Override
    protected List<ReactPackage> getPackages() {
      return Arrays.<ReactPackage>asList(
          new MainReactPackage(),
            new SunmiInnerPrinterPackage()
      );
    }
```

**Step 3:**

Import in React-Native:

```javascript
import SunmiV2Printer from 'react-native-sunmi-v2-printer';
```

## API

### Constants

| Name | Description|
|:-----:|:-----------:|
| Constants | 打印状态常量 |
| hasPrinter | boolean,是否有打印机 |
| printerVersion | 打印机固件版本 |
| printerSerialNo | 打印机序列号 |
| printerModal | 打印机型号 |

### Printer Status

|  Name | Description |
|:-----:|:-----------:|
| OUT_OF_PAPER_ACTION | 缺纸异常 |
| ERROR_ACTION | 打印错误 |
| NORMAL_ACTION | 可以打印 |
| COVER_OPEN_ACTION | 开盖子 |
| COVER_ERROR_ACTION | 关盖子异常 |
| KNIFE_ERROR_1_ACTION | 切刀异常1－卡切刀 |
| KNIFE_ERROR_2_ACTION | 切刀异常2－切刀修复 |
| OVER_HEATING_ACITON | 打印头过热异常 |
| FIRMWARE_UPDATING_ACITON | 打印机固件开始升级 |

### Example

Please check on `example/` floder
