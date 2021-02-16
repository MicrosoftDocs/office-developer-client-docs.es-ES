---
title: Agregar una definición para un nuevo campo definido por el usuario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428168"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="a7457-103">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="a7457-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="a7457-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7457-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7457-105">Cuando se agrega un campo definido por el usuario a un elemento de Microsoft Outlook, se agrega una definición de campo a la estructura de [secuencias PropertyDefinition](propertydefinition-stream-structure.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a7457-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="a7457-106">Use el siguiente procedimiento para agregar una nueva definición de campo a una estructura de secuencia PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a7457-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="a7457-107">Para agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="a7457-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="a7457-108">Copie las definiciones de campo existentes de la estructura de secuencia PropertyDefinition en una nueva matriz de definiciones de campo.</span><span class="sxs-lookup"><span data-stu-id="a7457-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="a7457-109">Si alguna definición de campo existente está en el formato PropDefV1, conviétalas al formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="a7457-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="a7457-110">Para obtener más información acerca de los formatos de definición de campo, vea [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) y [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a7457-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="a7457-111">Cree una definición del nuevo campo definido por el usuario en el formato PropDefV2 y agrégalo a la matriz.</span><span class="sxs-lookup"><span data-stu-id="a7457-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="a7457-112">Establece el elemento Version de la estructura de secuencias PropertyDefinition como 0x0103, si el elemento Version no se ha establecido en ese valor.</span><span class="sxs-lookup"><span data-stu-id="a7457-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="a7457-113">Incremente el elemento FieldDefinitionCount en 1.</span><span class="sxs-lookup"><span data-stu-id="a7457-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="a7457-114">Almacene la matriz como el valor del elemento FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="a7457-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7457-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a7457-115">See also</span></span>

- [<span data-ttu-id="a7457-116">Estructura de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7457-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

