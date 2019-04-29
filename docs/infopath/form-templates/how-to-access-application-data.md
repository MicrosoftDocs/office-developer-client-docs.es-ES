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
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417234"
---
# <a name="access-application-data"></a><span data-ttu-id="cd707-105">Datos de aplicaciones de Access</span><span class="sxs-lookup"><span data-stu-id="cd707-105">Access Application Data</span></span>

<span data-ttu-id="cd707-p102">El modelo de objetos de código administrado de InfoPath proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación de InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos, se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cd707-p102">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file. This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="cd707-108">En un proyecto de plantilla de formulario de código administrado de InfoPath creado con Visual Studio 2012, puede usar la palabra clave **this** (C#) o **Me** (Visual Basic) para tener acceso a una instancia de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que representa la aplicación InfoPath actual, que se puede utilizar para tener acceso a las propiedades y los métodos de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cd707-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cd707-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd707-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="cd707-110">Mostrar el nombre, la versión y el id. de idioma de la aplicación</span><span class="sxs-lookup"><span data-stu-id="cd707-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="cd707-p103">En el siguiente ejemplo, las propiedades [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) y [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) se utilizan para devolver el nombre y el número de versión de la instancia de InfoPath que se está ejecutando. La propiedad [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) se usa a continuación para devolver un objeto **LanguageSettings**, que a su vez se usa para devolver el LCID (un número de cuatro dígitos) del idioma que se está usando en ese momento en la interfaz de usuario de InfoPath. Por último, toda esta información se muestra en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd707-p103">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath. The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language. Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cd707-p104">[!IMPORTANTE] Para que funcione la propiedad **LanguageSettings**, debe establecer una referencia a la biblioteca de objetos de Microsoft Office 14.0 (desde la ficha **COM** del cuadro de diálogo **Agregar referencia** en Visual Studio 2012). Así, se establecerá una referencia al espacio de nombres **Microsoft.Office.Core**, que contiene la clase **LanguageSettings**. Además, el formulario se debe estar ejecutando como plena confianza.</span><span class="sxs-lookup"><span data-stu-id="cd707-p104">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012. This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class. Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="cd707-117">En este ejemplo, es necesaria una directiva **using** o **Imports** para el espacio de nombres **Microsoft.Office.Core** de la sección de declaraciones del módulo de código del formulario.</span><span class="sxs-lookup"><span data-stu-id="cd707-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
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


