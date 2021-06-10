---
title: Utilizar el Asistente para bibliotecas de tipos de Java
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a27491acabd19f688eca4159a36dcfcfc486a026
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312085"
---
# <a name="using-the-java-type-library-wizard"></a>Uso del Asistente para la biblioteca de tipos de Java


**Se aplica a:** Access 2013, Office 2013

El Asistente para bibliotecas de tipos de Java es una característica de Visual J++ 1.x integrada en el menú **Herramientas** del entorno de desarrollo. Su propósito es buscar en una biblioteca de tipos y crear una interfaz Java que permita obtener acceso a objetos COM. Para Visual J++ 6.0, el Asistente para bibliotecas de tipos de Java se ha reemplazado con [ADO para Windows Foundation Classes](ado-wfc-programming.md).

El Asistente para bibliotecas de tipos de Java genera resultados similares a las herramientas de línea de comandos incluidas en [Microsoft SDK para Java](using-the-microsoft-sdk-for-java.md). Sin embargo, no se pueden ejecutar paso a paso los contenedores de clase que genera el Asistente, a diferencia de los contenedores de clase generados por Microsoft SDK para Java.

El Java biblioteca de tipos genera las clases en la siguiente ubicación: directorio de \\ \< windows Java \> \\ \\ trustlib \\ msado15. El archivo Summary.txt, ubicado en el directorio donde se han generado las clases, muestra las definiciones de clase generadas.

El Asistente para bibliotecas de tipos de Java convierte los tipos enumerados, que se encuentran en cualquier biblioteca de tipos especificado, en el tipo INT (entero). También define una interfaz correspondiente a cada tipo enumerado en la biblioteca de tipos. Se puede hacer referencia a los valores de un tipo enumerado de ADO con la sintaxis siguiente:

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

Un ejemplo de esto aparece en el siguiente fragmento de código para establecer el valor de la propiedad **CommandType** de un objeto **Command**:

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

Asimismo, se puede heredar del contenedor de tipos enumerados generado por el Asistente para bibliotecas de tipos de Java. En ese caso, se puede quitar "msado15." de la sintaxis. Sin embargo, la clase deberá heredar de cada objeto Java e interfaz de tipos enumerados a los que haga referencia para que no sea necesario hacer referencia a msado15.\* delante de todos los valores enumerados y objetos de ADO.

Para obtener más código de ejemplo, vea [Contenedores de clase Java de ADO](ado-java-class-wrappers.md).

**Para ejecutar el Asistente Java biblioteca de tipos desde Visual J++ versión 1.*x***

1.  En el menú **Herramientas**, seleccione **Asistente para bibliotecas de tipos de Java**.

2.  Seleccione "Biblioteca de objetos de datos de Microsoft ActiveX" y haga clic en **Aceptar**. Esto ahora (re)genera archivos en el directorio trustlib para ADO (de forma predeterminada en \\ c: \\ winnt \\ java \\ trustlib \\ msado15). Si ha utilizado Microsoft SDK para Java para generar clases para ADO, éstas se reemplazarán con las clases del Asistente para bibliotecas de tipos de Java.

3.  Para utilizar estos archivos, abra un proyecto en Visual J++. En el menú **Proyecto**, elija **Agregar al proyecto**. Seleccione **Archivos** y agregue todos los archivos . Archivos JAVA generados en el directorio trustlib (de forma predeterminada \\ en c: \\ winnt \\ java \\ trustlib \\ msado15) para el proyecto.

