---
title: Estructuras de secuencia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581583"
---
# <a name="stream-structures"></a><span data-ttu-id="3cfb2-103">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="3cfb2-103">Stream Structures</span></span>

  
  
<span data-ttu-id="3cfb2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cfb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cfb2-105">Definiciones de campos definidos por el usuario de un elemento de Microsoft Outlook se almacenan en la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfb2-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="3cfb2-106">El valor de esta propiedad es una secuencia binaria que contiene las definiciones de campos definidos por el usuario y la configuración de enlace de datos para los campos integrados para el elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="3cfb2-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="3cfb2-107">En esta sección se proporciona información acerca de la estructura de la secuencia binaria, desglosada en las siguientes estructuras de secuencia.</span><span class="sxs-lookup"><span data-stu-id="3cfb2-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3cfb2-108">Los nombres de estas estructuras de secuencia (por ejemplo, PropertyDefinition, FieldDefinition y SkipBlock) y sus elementos de datos no son técnicamente forman parte de la interfaz de programación de la API de mensajería (MAPI) y se proporcionan aquí sólo para la documentación con fines de las estructuras de la secuencia real.</span><span class="sxs-lookup"><span data-stu-id="3cfb2-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="3cfb2-109">Los desarrolladores pueden etiquetar estos elementos de las estructuras y datos de secuencia en sus aplicaciones cuando lo prefieran.</span><span class="sxs-lookup"><span data-stu-id="3cfb2-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="3cfb2-110">Muestra de la secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="3cfb2-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="3cfb2-111">Muestra de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="3cfb2-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="3cfb2-112">Estructura de la secuencia SkipBlock</span><span class="sxs-lookup"><span data-stu-id="3cfb2-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="3cfb2-113">Estructura de la secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="3cfb2-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="3cfb2-114">Estructura de la secuencia PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="3cfb2-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="3cfb2-115">Estructura de la secuencia PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="3cfb2-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="3cfb2-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3cfb2-116">See also</span></span>



[<span data-ttu-id="3cfb2-117">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="3cfb2-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="3cfb2-118">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="3cfb2-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="3cfb2-119">Ejemplo de flujo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="3cfb2-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

