---
title: Propiedad canónica PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360743"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="5ddb5-103">Propiedad canónica PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="5ddb5-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="5ddb5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ddb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ddb5-105">Contiene el nombre, el tipo de datos y otra información sobre un campo definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ddb5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5ddb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ddb5-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="5ddb5-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="5ddb5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5ddb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ddb5-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="5ddb5-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="5ddb5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5ddb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ddb5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5ddb5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5ddb5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5ddb5-112">Area:</span></span>  <br/> |<span data-ttu-id="5ddb5-113">Carpeta MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddb5-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ddb5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ddb5-114">Remarks</span></span>

<span data-ttu-id="5ddb5-115">Para cada elemento, Outlook almacena las definiciones de todos los campos definidos por el usuario en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) del objeto **IMessage** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="5ddb5-116">La **propiedad PidLidPropertyDefinitionStream** contiene una secuencia binaria conocida como [PropertyDefinition](propertydefinition-stream-structure.md), que contiene las definiciones de campo.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="5ddb5-117">Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo, vea [Estructuras de secuencia](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="5ddb5-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="5ddb5-118">Para cada carpeta, Outlook almacena las definiciones de todos los campos definidos por el usuario en esa carpeta en la propiedad **PidTagUserFields** de un mensaje asociado de la clase de mensaje IPC.MS. REN. USERFIELDS: se supone que cada carpeta no contiene más de un mensaje de esta clase en su tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5ddb5-119">Es posible que el conjunto de campos definidos por el usuario de una carpeta no coincida necesariamente con los conjuntos de campos definidos por el usuario en cada uno de sus elementos.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="5ddb5-120">El conjunto de campos definidos por el usuario en una carpeta se muestra en varios lugares de la interfaz de usuario de Outlook, como el Seleccionador de campos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="5ddb5-121">La propiedad **PidTagUserFields** del mensaje contiene una secuencia binaria, **FolderUserFields**, que contiene las definiciones de campo de carpeta.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="5ddb5-122">Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo de carpeta, vea [Estructuras](folder-fields-stream-structures.md) de secuencia de campos de carpeta y el ejemplo de secuencia [FolderUserFields](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5ddb5-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="5ddb5-123">Título de sección</span><span class="sxs-lookup"><span data-stu-id="5ddb5-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ddb5-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="5ddb5-124">Protocol specifications</span></span>

<span data-ttu-id="5ddb5-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ddb5-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ddb5-126">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ddb5-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5ddb5-127">Header files</span></span>

<span data-ttu-id="5ddb5-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ddb5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ddb5-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5ddb5-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ddb5-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ddb5-130">See also</span></span>



[<span data-ttu-id="5ddb5-131">Elementos y campos de Outlook</span><span class="sxs-lookup"><span data-stu-id="5ddb5-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="5ddb5-132">Agregar una definición para un campo User-Defined nuevo</span><span class="sxs-lookup"><span data-stu-id="5ddb5-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="5ddb5-133">Ejemplo de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="5ddb5-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="5ddb5-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddb5-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ddb5-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddb5-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ddb5-136">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddb5-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ddb5-137">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5ddb5-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

