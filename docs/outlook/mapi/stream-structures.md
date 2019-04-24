---
title: Estructuras de secuencia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327443"
---
# <a name="stream-structures"></a><span data-ttu-id="e7b37-103">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="e7b37-103">Stream Structures</span></span>

  
  
<span data-ttu-id="e7b37-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7b37-105">Las definiciones de los campos definidos por el usuario de un elemento de Microsoft Outlook se almacenan en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b37-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="e7b37-106">El valor de esta propiedad es una secuencia binaria que contiene las definiciones de los campos definidos por el usuario y la configuración de enlace de datos para los campos integrados para el elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="e7b37-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="e7b37-107">En esta sección se proporciona información acerca de la estructura de la secuencia binaria, dividida en las siguientes estructuras de secuencias.</span><span class="sxs-lookup"><span data-stu-id="e7b37-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7b37-108">Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no forman parte técnicamente de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí solo para la documentación. propósito de las estructuras de Stream reales.</span><span class="sxs-lookup"><span data-stu-id="e7b37-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="e7b37-109">Los desarrolladores pueden etiquetar estas estructuras de secuencia y elementos de datos en sus aplicaciones según su elección.</span><span class="sxs-lookup"><span data-stu-id="e7b37-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="e7b37-110">Estructura de la secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7b37-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="e7b37-111">Estructura de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="e7b37-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="e7b37-112">Estructura de la secuencia SkipBlock</span><span class="sxs-lookup"><span data-stu-id="e7b37-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="e7b37-113">Estructura de la secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="e7b37-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="e7b37-114">Estructura de la secuencia PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="e7b37-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="e7b37-115">Estructura de la secuencia PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="e7b37-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="e7b37-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b37-116">See also</span></span>



[<span data-ttu-id="e7b37-117">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="e7b37-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="e7b37-118">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="e7b37-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="e7b37-119">Ejemplo de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7b37-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

