---
title: Objeto Property (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301193"
---
# <a name="property-object-dao"></a><span data-ttu-id="775a3-102">Objeto Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="775a3-102">Property object (DAO)</span></span>

<span data-ttu-id="775a3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="775a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="775a3-104">Un objeto **Property** representa una característica integrada o definida por el usuario de un objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="775a3-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="775a3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="775a3-105">Remarks</span></span>

<span data-ttu-id="775a3-p101">Todos los objetos DAO excepto los objetos **Connection** y **Error** contienen una colección **Properties** que tiene objetos **Property** correspondientes a propiedades integradas de dicho objeto DAO. Además, el usuario puede definir objetos **Property** y anexarlos a la colección **Properties** de ciertos objetos DAO. Estos objetos **Property** (que suelen denominarse simplemente propiedades) caracterizan de forma exclusiva dicha instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="775a3-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object. The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="775a3-109">Pueden crearse propiedades definidas por el usuario para los objetos siguientes:</span><span class="sxs-lookup"><span data-stu-id="775a3-109">You can create user-defined properties for the following objects:</span></span>

- <span data-ttu-id="775a3-110">Objetos **Database**, **Index**, **QueryDef** y **TableDef**</span><span class="sxs-lookup"><span data-stu-id="775a3-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

- <span data-ttu-id="775a3-111">Objetos **Field** de las colecciones **Fields** de los objetos **QueryDef** y **TableDef**</span><span class="sxs-lookup"><span data-stu-id="775a3-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="775a3-p102">Para agregar una propiedad definida por el usuario, utilice el método **CreateProperty** para crear un objeto **Property** con un valor de la propiedad **Name** único. Establezca las propiedades **Type** y **Value** del nuevo objeto **Property** y, después, anéxelo a la colección **Properties** del objeto correspondiente. El objeto al que se agrega la propiedad definida por el usuario debe estar anexado a una colección. Si se hace referencia a un objeto **Property** definido por el usuario que no esté anexado a una colección **Properties**, se producirá un error, de la misma manera que si se anexa un objeto **Property** definido por el usuario a una colección **Properties** que contenga un objeto **Property** con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="775a3-p102">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting. Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object. The object to which you are adding the user-defined property must already be appended to a collection. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="775a3-116">Se pueden eliminar propiedades definidas por el usuario de la colección **Properties**, pero no se pueden eliminar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="775a3-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="775a3-p103">[!NOTA] Un objeto **Property** definido por el usuario está asociado sólo con la instancia específica de un objeto. La propiedad no está definida para todas las instancias de objetos del tipo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="775a3-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="775a3-p104">La colección **Properties** de un objeto se puede usar para enumerar las propiedades integradas y definidas por el usuario del objeto. Para tratarlas, no es necesario saber de antemano qué propiedades existen exactamente o cuáles son sus características (propiedades **Name** y **Type**). Sin embargo, se producirá un error si intenta leer una propiedad de sólo escritura, como la propiedad **Password** de un objeto **Workspace** o si intenta leer o escribir en una propiedad en un contexto inadecuado, por ejemplo el valor de la propiedad **Value** de un objeto **Field** de la colección **Fields** de un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="775a3-p104">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties. You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them. However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="775a3-122">El objeto **Property** tiene también cuatro propiedades integradas:</span><span class="sxs-lookup"><span data-stu-id="775a3-122">The **Property** object also has four built-in properties:</span></span>

- <span data-ttu-id="775a3-123">La propiedad **Name**, un valor de tipo **String** que identifica la propiedad de forma única.</span><span class="sxs-lookup"><span data-stu-id="775a3-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

- <span data-ttu-id="775a3-124">La propiedad **Type**, un valor de tipo **Integer** que especifica el tipo de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="775a3-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

- <span data-ttu-id="775a3-125">La propiedad **Value**, un valor de tipo **Variant** que contiene el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="775a3-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

- <span data-ttu-id="775a3-p105">La propiedad **Inherited**, un valor de tipo **Boolean** que indica si la propiedad es heredada de otro objeto. Por ejemplo, un objeto **Field** de una colección **Fields** de un objeto **Recordset** puede heredar propiedades del objeto **TableDef** o **QueryDef** subyacentes.</span><span class="sxs-lookup"><span data-stu-id="775a3-p105">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object. For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="775a3-128">Para hacer referencia a un objeto **Property** integrado de una colección por su número ordinal o por su valor de la propiedad **Name**, utilice uno de los siguientes formatos de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="775a3-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="775a3-129">\*object\***. Propiedades**(0)</span><span class="sxs-lookup"><span data-stu-id="775a3-129">\*object\***.Properties**(0)</span></span>

- <span data-ttu-id="775a3-130">*object\***. Propiedades**("* nombre\*")</span><span class="sxs-lookup"><span data-stu-id="775a3-130">*object\***.Properties**("* name\*")</span></span>

- <span data-ttu-id="775a3-131">*object\*\*\*. Nombre de*\* \! \[\* las propiedades\*\]</span><span class="sxs-lookup"><span data-stu-id="775a3-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="775a3-132">Para una propiedad integrada, también se puede usar la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="775a3-132">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="775a3-133">*objeto*. *nombre*</span><span class="sxs-lookup"><span data-stu-id="775a3-133">*object*.*name*</span></span>

> [!NOTE]
> <span data-ttu-id="775a3-134">Para una propiedad definida por el usuario, debe usar el objeto *completo\***. Sintaxis Properties**("* name\*").</span><span class="sxs-lookup"><span data-stu-id="775a3-134">For a user-defined property, you must use the full *object\***.Properties**("* name\*") syntax.</span></span>

<span data-ttu-id="775a3-p106">Con los mismos formatos de sintaxis, también se puede hacer referencia a la propiedad **Value** de un objeto **Property**. El contexto de la referencia determinará si se está haciendo referencia al objeto **Property** en sí o a la propiedad **Value** del objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="775a3-p106">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

