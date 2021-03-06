---
title: Utilizar Microsoft SDK para Java
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d297d019602cef7b6fbc4f5b0125b87ef642213f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306001"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Uso de Microsoft SDK para Java


**Se aplica a:** Access 2013, Office 2013

Microsoft SDK para Java es el kit del programador para el entorno de Microsoft Internet Explorer. Proporciona herramientas, información y ejemplos para ayudar a desarrollar programas y applets Java basados en JDK 1.1 y en la máquina virtual Win32 de Microsoft (Microsoft VM). Microsoft SDK para Java no está ligado a Microsoft Visual J++.

La utilidad Jactivex.exe genera clases a partir de una biblioteca de tipos pero sólo se puede invocar en la línea de comandos. Esta característica no está integrada en el entorno de desarrollo de Visual J++. A diferencia de las clases generadas por el [Asistente para bibliotecas de tipos de Java](using-the-java-type-library-wizard.md), se pueden ejecutar paso a paso los contenedores de clase creados por SDK. Esto es útil a la hora de depurar la forma en que el código utiliza las clases contenedoras de ADO.

Este mecanismo lee la biblioteca de tipos de ADO y genera clases de las que se pueden crear instancias en la aplicación. Genera esas clases en la siguiente ubicación: \\ \< directorio de windows Java \> \\ \\ trustlib \\ msado15.

La creación de una aplicación de ADO en Java mediante Microsoft SDK para Java es fundamentalmente idéntica, desde el punto de visto del código fuente, a utilizar el Asistente para bibliotecas de tipos de Java. Para obtener código de ejemplo, vea [Contenedores de clase Java de ADO](ado-java-class-wrappers.md). La única diferencia reside realmente en cómo se generan las clases contenedoras, tal y como se muestra en los pasos siguientes.

**Para crear un proyecto de ADO con Microsoft SDK para Java**

1.  Ejecute el siguiente comando en un símbolo del sistema. La ruta de acceso debe incluir el directorio Bin de Microsoft SDK para Java, o bien, es preciso ejecutar el comando desde esa ubicación. Microsoft SDK para Java suele estar instalado en la misma ubicación que Visual Studio. Se trata de una instrucción de un solo comando.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Ejecute el siguiente comando para compilar las clases generadas. El modificador /g:t activa la generación de símbolos de depuración para que se pueda realizar un seguimiento de los símbolos de .Java. Quítelo para las versiones de lanzamiento.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Para utilizar estos archivos, abra un proyecto en Visual J++. En el menú **Proyecto**, elija **Agregar al proyecto**. Seleccione **Archivos** y agregue todos los archivos . Archivos JAVA generados en el directorio \\ msado15 de trustlib para el proyecto.

