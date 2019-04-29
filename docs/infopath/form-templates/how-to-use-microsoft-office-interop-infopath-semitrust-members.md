---
title: Usar los miembros de Microsoft. Office. Interop. InfoPath. semiTrust no son compatibles con InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- plantillas de formulario compatibles con InfoPath 2003, mediante las características de InfoPath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: El modelo de objetos proporcionado por el espacio de nombres Microsoft. Office. Interop. InfoPath. semiTrust incluye objetos y miembros que proporcionan nueva funcionalidad que se agregó a Office InfoPath 2007 e InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415344"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="578b9-104">Usar los miembros de Microsoft. Office. Interop. InfoPath. semiTrust no son compatibles con InfoPath</span><span class="sxs-lookup"><span data-stu-id="578b9-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="578b9-105">Al agregar código a una plantilla de formulario creada con el kit de herramientas de Microsoft Office InfoPath 2003 o crear una nueva plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003 (como se describe en [crear una plantilla de formulario con el objeto infopath 2003 Modelo](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), de forma predeterminada, Microsoft InfoPath usará un subconjunto de los objetos y miembros proporcionados por el espacio de nombres [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , idénticos a los que se usan en InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="578b9-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="578b9-106">Esto se hace así para ofrecer compatibilidad con InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="578b9-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="578b9-107">Sin embargo, el modelo de objetos proporcionado por el espacio de nombres [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) incluye objetos y miembros adicionales que proporcionan nueva funcionalidad que se agregó a Office InfoPath 2007 e InfoPath.</span><span class="sxs-lookup"><span data-stu-id="578b9-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="578b9-108">Por ejemplo, las interfaces de [permisos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) y [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) proporcionan una nueva funcionalidad de Information Rights Management que no está disponible en InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="578b9-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="578b9-109">Esto y otros nuevos objetos agregados al espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust no están disponibles de manera predeterminada cuando abre o crea plantillas de formulario con código administrado con el modelo de objetos compatible con InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="578b9-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="578b9-110">De forma similar, mientras que la interfaz [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) proporciona la misma funcionalidad que InfoPath 2003; la interfaz [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) se ha asignado a una versión para incluir propiedades y métodos adicionales que se agregaron en Office InfoPath 2007, y el [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) se ha asignado a una versión para incluir propiedades y métodos adicionales que se agregaron en InfoPath .</span><span class="sxs-lookup"><span data-stu-id="578b9-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="578b9-111">Si desea usar objetos y miembros que se agregaron en Office InfoPath 2007 o InfoPath en un proyecto de plantilla de formulario creado mediante el modelo de objetos proporcionado por el espacio de nombres **Microsoft. Office. Interop. InfoPath. SemiTrust** , puede hacerlo, pero el código que usa Estos miembros no serán compatibles con InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="578b9-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="578b9-112">No se admiten todas las plantillas de formulario con lógica empresarial creada con el modelo de objetos proporcionado por el espacio de nombres **Microsoft. Office. Interop. InfoPath. SemiTrust** , ya sea que usen objetos y miembros compatibles con InfoPath o not, para plantillas de formulario habilitadas para el explorador implementadas en Microsoft SharePoint Server 2010 con InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="578b9-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="578b9-113">La lógica empresarial de las plantillas de formulario habilitadas para el explorador debe usar el nuevo modelo de objetos de código administrado de InfoPath proporcionado por el espacio de nombres [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="578b9-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="578b9-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="578b9-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="578b9-115">Crear un XDocument o una variable de objeto de aplicación para tener acceso a los miembros del nuevo modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="578b9-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="578b9-116">Para tener acceso a los nuevos objetos y miembros disponibles en el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust**, debe declarar y convertir variables de objetos en la versión correcta de la interfaz que implementa estos miembros.</span><span class="sxs-lookup"><span data-stu-id="578b9-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="578b9-117">De forma predeterminada, `thisXDocument` las `thisApplication` variables y tienen acceso a las versiones compatibles con InfoPath 2003 de las interfaces **_XDocument2** y [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="578b9-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="578b9-118">Para obtener acceso a las interfaces **_XDocument3** y [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) que proporcionan acceso a nuevas funciones, debe declarar una variable de objeto del tipo **_XDocument3** o **_Application3** y, a continuación, convertir el objeto devuelto por el `thisXDocument`o `thisApplication` variable en el mismo tipo, tal y como se muestra en los siguientes ejemplos.</span><span class="sxs-lookup"><span data-stu-id="578b9-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="578b9-119">Acceso a un nuevo objeto desde el XDocument o la variable de objeto de aplicación usando una propiedad de descriptor de acceso</span><span class="sxs-lookup"><span data-stu-id="578b9-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="578b9-120">Una vez que haya creado una variable de la versión más reciente _ **XDocument3** o **_Application3** tipo, puede usarla para tener acceso a un objeto o miembro que proporcione nuevas funciones de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="578b9-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="578b9-121">En el ejemplo siguiente se muestra cómo usar una variable de objeto de tipo _ **XDocument3** con la propiedad de descriptor de acceso de [permiso](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) para obtener acceso a la nueva interfaz **Permission** y a su propiedad [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) para determinar si la configuración de los permisos es habilitado para el formulario.</span><span class="sxs-lookup"><span data-stu-id="578b9-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="578b9-122">Acceso a un objeto con otra versión y conversión en el tipo de la versión</span><span class="sxs-lookup"><span data-stu-id="578b9-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="578b9-123">Si un objeto que existía en el modelo de objetos de InfoPath 2003 tiene ahora nuevas propiedades o métodos agregados, el objeto que los implemente tendrá un nombre que esté en la versión.</span><span class="sxs-lookup"><span data-stu-id="578b9-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="578b9-124">Por ejemplo, el objeto [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) no proporciona acceso a dos nuevas propiedades que solo están disponibles cuando se usa el objeto [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) con versión: las propiedades [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) y [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="578b9-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="578b9-125">Para tener acceso a estas propiedades, debe declarar una variable de objeto de tipo **ViewInfo2** y convertir el objeto devuelto por la propiedad [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) de la variable de objeto _ **XDocument3** en el tipo **ViewInfo2** , tal y como se muestra en la siguiente siguiente.</span><span class="sxs-lookup"><span data-stu-id="578b9-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
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


