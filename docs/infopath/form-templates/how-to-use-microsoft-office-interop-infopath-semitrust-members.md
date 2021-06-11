---
title: Use Microsoft. Office.Interop.InfoPath.SemiTrust miembros no compatibles con InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Plantillas de formulario compatibles con infopath 2003, con características de infopath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Modelo de objetos proporcionado por Microsoft. Office.Interop.InfoPath.SemiTrust espacio de nombres incluye objetos y miembros que proporcionan nueva funcionalidad que se agregó a Office InfoPath 2007 e InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415344"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Use Microsoft. Office.Interop.InfoPath.SemiTrust miembros no compatibles con InfoPath

Al agregar código a una plantilla de formulario creada con el Toolkit de InfoPath 2003 de Microsoft Office o crear una nueva plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003 (como se describe en Crear una plantilla de formulario mediante el modelo de objetos de [InfoPath 2003),](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)de forma predeterminada, Microsoft InfoPath usará un subconjunto de los objetos y miembros proporcionados por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que son idénticos a los usados por InfoPath 2003. Esto se hace así para ofrecer compatibilidad con InfoPath 2003. Sin embargo, el modelo de objetos proporcionado por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) incluye objetos y miembros adicionales que proporcionan nuevas funciones que se agregaron a Office InfoPath 2007 e InfoPath. 
  
Por ejemplo, las interfaces [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) y [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) proporcionan nuevas funciones de administración de derechos de información que no están disponibles en InfoPath 2003. Esto y otros nuevos objetos agregados al espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust no están disponibles de manera predeterminada cuando abre o crea plantillas de formulario con código administrado con el modelo de objetos compatible con InfoPath 2003. 
  
Del mismo modo, mientras que [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interfaz proporciona la misma funcionalidad que InfoPath 2003; la [interfaz _XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) se ha versionado para incluir propiedades y métodos adicionales que se agregaron en Office InfoPath 2007 y el [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) se ha versionado para incluir propiedades y métodos adicionales que se agregaron en InfoPath. 
  
Si desea usar objetos y miembros que se agregaron en Office InfoPath 2007 o InfoPath en un proyecto de plantilla de formulario creado con el modelo de objetos proporcionado por el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust,** puede hacerlo, pero el código que usa estos miembros no será compatible con InfoPath 2003. 
  
> [!NOTE]
> Todas las plantillas de formulario con lógica empresarial creadas con el modelo de objetos proporcionado por el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust,** tanto si usan objetos como miembros compatibles con InfoPath o no, no se admiten en las plantillas de formulario habilitadas para explorador implementadas en Microsoft SharePoint Server 2010 con InfoPath Forms Services. La lógica empresarial de las plantillas de formulario habilitadas para explorador debe usar el nuevo modelo de objetos de código administrado de InfoPath proporcionado por [Microsoft.Office. Espacio de nombres de InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
## <a name="example"></a>Ejemplo

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Crear un XDocument o una variable de objeto de aplicación para tener acceso a los miembros del nuevo modelo de objetos

Para tener acceso a los nuevos objetos y miembros disponibles en el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust**, debe declarar y convertir variables de objetos en la versión correcta de la interfaz que implementa estos miembros. De forma predeterminada, las variables y tienen acceso a las versiones compatibles con `thisXDocument` `thisApplication` InfoPath 2003  de las interfaces _XDocument2 y [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) correspondientes. Para obtener acceso a las interfaces **_XDocument3** y [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) que proporcionan acceso a nuevas funciones, debe declarar una variable de objeto del tipo **_XDocument3** o _Application3 y, **a** continuación, convertir el objeto devuelto por la variable or al mismo tipo que se muestra en los ejemplos  `thisXDocument`  `thisApplication` siguientes. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>Acceso a un nuevo objeto desde el XDocument o la variable de objeto de aplicación usando una propiedad de descriptor de acceso

Después de crear una variable de la versión posterior _ **XDocument3** o **_Application3,** puede usarla para obtener acceso a un objeto o miembro que proporciona nuevas funciones de InfoPath. 
  
En el ejemplo siguiente se muestra cómo usar una variable de objeto de tipo _ **XDocument3** con la propiedad [accessor](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) Permission para obtener acceso a la nueva interfaz **Permission** y su [propiedad Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) para determinar si la configuración de permisos está habilitada para el formulario. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>Acceso a un objeto con otra versión y conversión en el tipo de la versión

Si un objeto que existía en el modelo de objetos de InfoPath 2003 tiene ahora nuevas propiedades o métodos agregados, el objeto que los implemente tendrá un nombre que esté en la versión.
  
Por ejemplo, el [objeto ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) no proporciona acceso a dos nuevas propiedades que solo están disponibles cuando se usa el objeto [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) con versiones: las propiedades [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) y [HideName.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) 
  
Para obtener acceso a estas propiedades, debe declarar una variable de objeto de tipo **ViewInfo2** y convertir el objeto devuelto por la propiedad [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) de la variable de objeto _ **XDocument3** en el tipo **ViewInfo2** como se muestra en el ejemplo siguiente. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


