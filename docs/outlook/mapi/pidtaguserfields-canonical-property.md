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
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820407"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="f094d-103">Propiedad canónica PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="f094d-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="f094d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f094d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f094d-105">Contiene el nombre, tipo de datos y otra información acerca de un campo definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f094d-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f094d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f094d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f094d-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="f094d-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="f094d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f094d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f094d-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="f094d-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="f094d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f094d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f094d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f094d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f094d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f094d-112">Area:</span></span>  <br/> |<span data-ttu-id="f094d-113">Carpeta MAPI</span><span class="sxs-lookup"><span data-stu-id="f094d-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f094d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f094d-114">Remarks</span></span>

<span data-ttu-id="f094d-115">Para cada elemento, Outlook almacena las definiciones de todos los campos definidos por el usuario en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) del objeto **IMessage** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f094d-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="f094d-116">La propiedad **PidLidPropertyDefinitionStream** contiene una secuencia binaria conocida como [PropertyDefinition](propertydefinition-stream-structure.md), que contiene las definiciones de campo.</span><span class="sxs-lookup"><span data-stu-id="f094d-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="f094d-117">Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo, vea [Estructuras de secuencia](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="f094d-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="f094d-118">Para cada carpeta, Outlook almacena las definiciones de todos los campos definidos por el usuario en esa carpeta en la propiedad **PidTagUserFields** de un mensaje asociado de la clase de mensaje IPC.MS. REN. USERFIELDS - supone que cada carpeta para contener no más de un mensaje de esta clase en su tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="f094d-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f094d-119">El conjunto de campos definidos por el usuario en una carpeta no es posible que necesariamente deben coincidir con los conjuntos de campos definidos por el usuario en cada uno de sus elementos.</span><span class="sxs-lookup"><span data-stu-id="f094d-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="f094d-120">El conjunto de campos definidos por el usuario en una carpeta se muestra en diversos lugares de la interfaz de usuario de Outlook, como el selector de campos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f094d-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="f094d-121">La propiedad del mensaje **PidTagUserFields** contiene una secuencia binaria, **FolderUserFields**, que contiene las definiciones de campo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f094d-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="f094d-122">Para obtener más información acerca de las estructuras de secuencia para las definiciones de campo de carpeta, vea [Estructuras de secuencia de los campos de carpeta](folder-fields-stream-structures.md) y el [Ejemplo de secuencia de FolderUserFields](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f094d-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="f094d-123">Encabezado de sección</span><span class="sxs-lookup"><span data-stu-id="f094d-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f094d-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f094d-124">Protocol specifications</span></span>

<span data-ttu-id="f094d-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f094d-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f094d-126">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f094d-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f094d-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f094d-127">Header files</span></span>

<span data-ttu-id="f094d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f094d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f094d-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f094d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f094d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f094d-130">See also</span></span>



[<span data-ttu-id="f094d-131">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="f094d-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="f094d-132">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="f094d-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="f094d-133">Ejemplo de flujo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f094d-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="f094d-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f094d-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f094d-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f094d-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f094d-136">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f094d-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f094d-137">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f094d-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

