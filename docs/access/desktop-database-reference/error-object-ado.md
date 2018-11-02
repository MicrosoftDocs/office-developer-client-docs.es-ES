---
title: Objeto Error - ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6a18570071428bfbd92d6674ca281234ea883bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925215"
---
# <a name="error-object-ado"></a><span data-ttu-id="4f9d9-102">Error (objeto, ADO)</span><span class="sxs-lookup"><span data-stu-id="4f9d9-102">Error object (ADO)</span></span>


<span data-ttu-id="4f9d9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f9d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f9d9-104">Contiene detalles sobre errores de acceso a datos relacionados con una operación única que implica al proveedor.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-104">Contains details about data access errors that pertain to a single operation involving the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f9d9-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f9d9-105">Remarks</span></span>

<span data-ttu-id="4f9d9-p101">Toda operación que implique a objetos de ADO puede generar errores relacionados con el proveedor. Cuando se produce alguno de estos errores, se colocan objetos **Error** en la colección [Errors](errors-collection-ado.md) del objeto [Connection](connection-object-ado.md). Cuando otra operación ADO genera un error, se borra la colección **Errors** y el nuevo conjunto de objetos **Error** se coloca en la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the [Errors](errors-collection-ado.md) collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="4f9d9-p102">[!NOTA] Cada objeto **Error** representa un error de proveedor específico, no un error de ADO. Los errores de ADO se exponen al mecanismo de control de excepciones en tiempo de ejecución. Por ejemplo, en Microsoft Visual Basic, la generación de un error específico de ADO desencadenará un evento **On Error** y aparecerá el objeto **Error**. Para obtener una lista completa de errores de ADO, vea el tema correspondiente a [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an **On Error** event and appear in the **Error** object. For a complete list of ADO errors, see the [ErrorValueEnum](errorvalueenum.md) topic.</span></span>

<span data-ttu-id="4f9d9-113">Puede leer las propiedades de un objeto **Error** para obtener detalles específicos de cada error, como por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4f9d9-113">You can read an **Error** object's properties to obtain specific details about each error, including the following:</span></span>

- <span data-ttu-id="4f9d9-p103">La propiedad [Description](description-property-ado.md), que contiene el texto del error. Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p103">The [Description](description-property-ado.md) property, which contains the text of the error. This is the default property.</span></span>

- <span data-ttu-id="4f9d9-116">La propiedad [Number](number-property-ado.md), que contiene al valor entero de tipo **Long** de la constante del error.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-116">The [Number](number-property-ado.md) property, which contains the **Long** integer value of the error constant.</span></span>

- <span data-ttu-id="4f9d9-p104">La propiedad [Source](source-property-ado-error.md), que identifica el objeto que generó el error. Esto es sumamente útil cuando se tienen varios objetos **Error** en la colección **Errors** tras realizar una solicitud a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p104">The [Source](source-property-ado-error.md) property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to a data source.</span></span>

- <span data-ttu-id="4f9d9-119">Las propiedades [SQLState](sqlstate-property-ado.md) y [NativeError](nativeerror-property-ado.md), que proporcionan información de orígenes de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-119">The [SQLState](sqlstate-property-ado.md) and [NativeError](nativeerror-property-ado.md) properties, which provide information from SQL data sources.</span></span>

<span data-ttu-id="4f9d9-p105">Cuando se produce un error de proveedor, se coloca en la colección **Errors** del objeto **Connection**. ADO admite la devolución de varios errores mediante una única operación de ADO para proporcionar información específica de errores al proveedor. Para obtener esta valiosa información de errores en un controlador de errores, utilice las características de intercepción de errores apropiadas del lenguaje o del entorno con el que está trabajando y, a continuación, use bucles anidados para enumerar las propiedades de cada objeto **Error** de la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p105">When a provider error occurs, it is placed in the **Errors** collection of the **Connection** object. ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider. To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each **Error** object in the **Errors** collection.</span></span>

<span data-ttu-id="4f9d9-123">**Microsoft Visual Basic y VBScript a los usuarios** Si no hay ningún objeto **Connection** válido, debe recuperar información de errores desde el objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="4f9d9-123">**Microsoft Visual Basic and VBScript Users**If there is no valid **Connection** object, you will need to retrieve error information from the **Error** object.</span></span>

<span data-ttu-id="4f9d9-p106">Del mismo modo que hacen los proveedores, ADO borra el objeto **OLE Error Info** antes de realizar una llamada que pueda generar un nuevo error de proveedor. Sin embargo, la colección **Errors** del objeto **Connection** se borra y se rellena sólo cuando el proveedor genera un nuevo error, o cuando se llama al método [Clear](clear-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p106">Just as providers do, ADO clears the **OLE Error Info** object before making a call that could potentially generate a new provider error. However, the **Errors** collection on the **Connection** object is cleared and populated only when the provider generates a new error, or when the [Clear](clear-method-ado.md) method is called.</span></span>

<span data-ttu-id="4f9d9-p107">Algunos métodos y propiedades devuelven advertencias que aparecen como objetos **Error** en la colección **Errors** pero que no detienen la ejecución de un programa. Antes de llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) en un objeto [Recordset](recordset-object-ado.md), antes de llamar al método [Open](open-method-ado-connection.md) en un objeto **Connection**, y antes de establecer la propiedad [Filter](filter-property-ado.md) en un objeto **Recordset**, llame al método **Clear** en la colección **Errors**. De este modo, podrá leer la propiedad [Count](count-property-ado.md) de la colección **Errors** y comprobar si se devuelven advertencias.</span><span class="sxs-lookup"><span data-stu-id="4f9d9-p107">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a **Connection** object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

