---
title: Campos y elementos de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: caa231842c5fd51deb80144f12fdf53e51ccc980
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582878"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="f6345-103">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="f6345-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="f6345-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6345-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6345-105">Microsoft Outlook proporciona los tipos de elementos que están especializados para su funcionalidad (por ejemplo, elementos de correo, citas, contactos, tareas y notas).</span><span class="sxs-lookup"><span data-stu-id="f6345-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="f6345-106">Outlook proporciona campos estándar para cada tipo de elemento, comúnmente como campos integrados.</span><span class="sxs-lookup"><span data-stu-id="f6345-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="f6345-107">Outlook también permite a los usuarios crear campos personalizados, comúnmente como campos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f6345-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="f6345-108">Cada campo está asociado con un tipo de datos y un valor.</span><span class="sxs-lookup"><span data-stu-id="f6345-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="f6345-109">Ejemplos de tipos de datos son **moneda**, **Fecha y hora**, **duración**, **número entero**, **palabras clave**y **texto**.</span><span class="sxs-lookup"><span data-stu-id="f6345-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="f6345-110">Los usuarios pueden definir campos personalizados mediante el Diseñador de formularios de Outlook.</span><span class="sxs-lookup"><span data-stu-id="f6345-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="f6345-111">En el nivel de programación, cada elemento está representado por un objeto [IMessage](imessageimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="f6345-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="f6345-112">Cada campo definido por el usuario está asociado con una definición de campo y un valor.</span><span class="sxs-lookup"><span data-stu-id="f6345-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="f6345-113">Definición de campo</span><span class="sxs-lookup"><span data-stu-id="f6345-113">Field Definition</span></span>

<span data-ttu-id="f6345-114">Una definición de campo incluye el nombre, tipo de datos y otra información acerca del campo.</span><span class="sxs-lookup"><span data-stu-id="f6345-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="f6345-115">Para cada elemento, Outlook almacena las definiciones de todos los campos definidos por el usuario en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) del objeto **IMessage** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f6345-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="f6345-116">La propiedad **PidLidPropertyDefinitionStream** contiene una secuencia binaria conocida como [PropertyDefinition](propertydefinition-stream-structure.md) que contiene las definiciones de campo.</span><span class="sxs-lookup"><span data-stu-id="f6345-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="f6345-117">Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo, vea [Estructuras de secuencia](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="f6345-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="f6345-118">Valor de campo</span><span class="sxs-lookup"><span data-stu-id="f6345-118">Field Value</span></span>

<span data-ttu-id="f6345-119">Cada campo definido por el usuario de un elemento tiene un valor que se almacena en una propiedad con nombre correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f6345-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="f6345-120">Que la propiedad con nombre se encuentra en el conjunto de propiedades PS_PUBLIC_STRINGS y tiene una cadena de caracteres Unicode como el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f6345-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="f6345-121">El tipo de datos de la propiedad corresponde al tipo del campo.</span><span class="sxs-lookup"><span data-stu-id="f6345-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="f6345-122">Si la propiedad no está presente en el objeto **IMessage** , Outlook supone un valor predeterminado razonable para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f6345-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="f6345-123">Por ejemplo, para un tipo de cadena, Outlook supone una cadena vacía si la propiedad no está presente.</span><span class="sxs-lookup"><span data-stu-id="f6345-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6345-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6345-124">See also</span></span>



[<span data-ttu-id="f6345-125">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="f6345-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="f6345-126">Ejemplo de flujo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6345-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="f6345-127">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="f6345-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="f6345-128">Muestra de la secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6345-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="f6345-129">Muestra de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="f6345-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="f6345-130">Estructura de la secuencia SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f6345-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="f6345-131">Estructura de la secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="f6345-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="f6345-132">Estructura de la secuencia PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="f6345-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="f6345-133">Estructura de la secuencia PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="f6345-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

