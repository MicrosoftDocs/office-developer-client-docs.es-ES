---
title: Datos de aplicaciones de Access
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- application names [infopath 2007],accessing application name [InfoPath 2007],InfoPath 2007, accessing application data,accessing application version [InfoPath 2007],application versions [InfoPath 2007],language IDs [InfoPath 2007],LCID [InfoPath 2007],application data [InfoPath 2007],accessing language ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: El modelo de objetos de código administrado de InfoPath proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación de InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos, se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la clase Application .
ms.openlocfilehash: 3c3f6be4e90e292eb572da836bca0a8dcf1883cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815853"
---
# <a name="access-application-data"></a>Datos de aplicaciones de Access

El modelo de objetos de código administrado de InfoPath proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación de InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos, se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
En un proyecto de plantilla de formulario de código administrado de InfoPath creado con Visual Studio 2012, puede usar la palabra clave **this** (C#) o **Me** (Visual Basic) para tener acceso a una instancia de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que representa la aplicación InfoPath actual, que se puede utilizar para tener acceso a las propiedades y los métodos de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
## <a name="example"></a>Ejemplo

### <a name="displaying-the-application-name-version-and-language-id"></a>Mostrar el nombre, la versión y el id. de idioma de la aplicación

En el siguiente ejemplo, las propiedades [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) y [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) se utilizan para devolver el nombre y el número de versión de la instancia de InfoPath que se está ejecutando. La propiedad [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) se usa a continuación para devolver un objeto **LanguageSettings**, que a su vez se usa para devolver el LCID (un número de cuatro dígitos) del idioma que se está usando en ese momento en la interfaz de usuario de InfoPath. Por último, toda esta información se muestra en un cuadro de mensaje. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Para que funcione la propiedad **LanguageSettings**, debe establecer una referencia a la biblioteca de objetos de Microsoft Office 14.0 (desde la ficha **COM** del cuadro de diálogo **Agregar referencia** en Visual Studio 2012). Así, se establecerá una referencia al espacio de nombres **Microsoft.Office.Core**, que contiene la clase **LanguageSettings**. Además, el formulario se debe estar ejecutando como plena confianza. 
  
En este ejemplo, es necesaria una directiva **using** o **Imports** para el espacio de nombres **Microsoft.Office.Core** de la sección de declaraciones del módulo de código del formulario. 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


