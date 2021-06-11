---
title: Estructura de secuencia PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438592"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="5c672-103">Estructura de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c672-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="5c672-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c672-105">Una estructura de secuencia PropertyDefinition es una matriz de estructuras de secuencia [FieldDefinition](fielddefinition-stream-structure.md) que contienen definiciones para todos los campos definidos por el usuario en un elemento de Microsoft Outlook y la configuración de enlace de datos para algunos campos integrados.</span><span class="sxs-lookup"><span data-stu-id="5c672-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="5c672-106">Puede manipular mediante programación la estructura de secuencia PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="5c672-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="5c672-107">Sin embargo, puede obtener resultados similares mediante el Diseñador de  formularios Outlook y, en particular, el cuadro de diálogo Propiedades de un control enlazado a datos.</span><span class="sxs-lookup"><span data-stu-id="5c672-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="5c672-108">Las definiciones de campo de una estructura de secuencia PropertyDefinition pueden ser de dos formatos: PropDefV1 y PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="5c672-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="5c672-109">Outlook es compatible con PropDefV1 y PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="5c672-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="5c672-110">Todas las definiciones de campo de una sola estructura de secuencia PropertyDefinition deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="5c672-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="5c672-111">Para obtener más información acerca de la diferencia entre PropDefV1 y PropDefV2, vea [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5c672-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="5c672-112">Los elementos de datos de esta secuencia se almacenan en el orden de bytes little-endian, siguiendo inmediatamente entre sí en el orden especificado a continuación.</span><span class="sxs-lookup"><span data-stu-id="5c672-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="5c672-113">Versión: WORD (2 bytes), el formato de las definiciones de campo en la estructura de secuencia PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="5c672-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="5c672-114">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5c672-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="5c672-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5c672-115">**Value**</span></span>|<span data-ttu-id="5c672-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c672-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="5c672-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="5c672-117">0x0102</span></span>  <br/> |<span data-ttu-id="5c672-118">Format es PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="5c672-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="5c672-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="5c672-119">0x0103</span></span>  <br/> |<span data-ttu-id="5c672-120">Format es PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="5c672-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="5c672-121">FieldDefinitionCount: DWORD (4 bytes), el número de definiciones de campo en esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="5c672-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="5c672-122">Este es el recuento de elementos de matriz en el elemento de datos FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="5c672-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="5c672-123">FieldDefinitions: una matriz de estructuras de secuencias FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="5c672-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="5c672-124">El recuento de esta matriz es igual al elemento de datos FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="5c672-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c672-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c672-125">See also</span></span>

- [<span data-ttu-id="5c672-126">Outlook Elementos y campos</span><span class="sxs-lookup"><span data-stu-id="5c672-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="5c672-127">Agregar una definición para un nuevo User-Defined campo</span><span class="sxs-lookup"><span data-stu-id="5c672-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="5c672-128">Ejemplo de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c672-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="5c672-129">Estructuras de secuencias</span><span class="sxs-lookup"><span data-stu-id="5c672-129">Stream Structures</span></span>](stream-structures.md)

