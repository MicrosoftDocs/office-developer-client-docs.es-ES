---
title: Agregue una definición para un nuevo campo definido por el usuario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816965"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="cec3c-103">Agregue una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="cec3c-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="cec3c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cec3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cec3c-105">Cuando se agrega un campo definido por el usuario a un elemento de Microsoft Outlook, agregue una definición de campo en la estructura de secuencia [PropertyDefinition](propertydefinition-stream-structure.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cec3c-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="cec3c-106">Use el procedimiento siguiente para agregar una nueva definición de campo a una estructura de secuencia PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cec3c-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="cec3c-107">Para agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="cec3c-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="cec3c-108">Copie las definiciones de campo existente de la estructura de la secuencia de PropertyDefinition en una matriz de definiciones de campo nuevo.</span><span class="sxs-lookup"><span data-stu-id="cec3c-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="cec3c-109">Si las definiciones de campo existente que se encuentran en el formato PropDefV1, convertirlos al formato de PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="cec3c-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="cec3c-110">Para obtener más información acerca de los formatos de definición de campo, vea [PropertyDefinition secuencia estructura](propertydefinition-stream-structure.md) y la [Estructura de la secuencia de FieldDefinition](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="cec3c-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="cec3c-111">Crear una definición del nuevo campo definido por el usuario en el formato PropDefV2 y agregarlo a la matriz.</span><span class="sxs-lookup"><span data-stu-id="cec3c-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="cec3c-112">Establezca el elemento de versión de la estructura de la secuencia de PropertyDefinition como 0 x 0103, si el elemento Version no se ha establecido para ese valor.</span><span class="sxs-lookup"><span data-stu-id="cec3c-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="cec3c-113">Incrementar el elemento FieldDefinitionCount en 1.</span><span class="sxs-lookup"><span data-stu-id="cec3c-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="cec3c-114">Almacenar la matriz como el valor del elemento FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="cec3c-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cec3c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="cec3c-115">See also</span></span>

- [<span data-ttu-id="cec3c-116">Muestra de la secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="cec3c-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
