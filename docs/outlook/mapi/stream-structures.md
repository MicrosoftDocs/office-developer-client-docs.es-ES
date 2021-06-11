---
title: Estructuras de secuencias
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407826"
---
# <a name="stream-structures"></a><span data-ttu-id="be81d-103">Estructuras de secuencias</span><span class="sxs-lookup"><span data-stu-id="be81d-103">Stream Structures</span></span>

  
  
<span data-ttu-id="be81d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be81d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be81d-105">Las definiciones de campos definidos por el usuario de un elemento Outlook microsoft se almacenan en la [propiedad PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="be81d-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="be81d-106">El valor de esta propiedad es una secuencia binaria que contiene definiciones de campos definidos por el usuario y opciones de enlace de datos para los campos integrados para el Outlook elemento.</span><span class="sxs-lookup"><span data-stu-id="be81d-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="be81d-107">En esta sección se proporciona información sobre la estructura de la secuencia binaria, desglosada en las siguientes estructuras de secuencia.</span><span class="sxs-lookup"><span data-stu-id="be81d-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="be81d-108">Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no forman parte técnicamente de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí solo con fines de documentación de las estructuras de secuencias reales.</span><span class="sxs-lookup"><span data-stu-id="be81d-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="be81d-109">Los desarrolladores pueden etiquetar estas estructuras de secuencia y los elementos de datos en sus aplicaciones según lo elijan.</span><span class="sxs-lookup"><span data-stu-id="be81d-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="be81d-110">Estructura de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="be81d-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="be81d-111">Estructura de secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="be81d-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="be81d-112">Estructura de secuencias SkipBlock</span><span class="sxs-lookup"><span data-stu-id="be81d-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="be81d-113">Estructura de secuencias FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="be81d-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="be81d-114">Estructura de secuencias PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="be81d-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="be81d-115">Estructura de secuencias PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="be81d-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="be81d-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="be81d-116">See also</span></span>



[<span data-ttu-id="be81d-117">Outlook Elementos y campos</span><span class="sxs-lookup"><span data-stu-id="be81d-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="be81d-118">Agregar una definición para un nuevo User-Defined campo</span><span class="sxs-lookup"><span data-stu-id="be81d-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="be81d-119">Ejemplo de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="be81d-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

