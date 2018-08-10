---
title: Estructura de la secuencia de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820467"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="ad0ff-103">Estructura de la secuencia de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="ad0ff-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="ad0ff-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad0ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad0ff-105">Una estructura de secuencia PropertyDefinition es una matriz de estructuras de secuencia [FieldDefinition](fielddefinition-stream-structure.md) que contienen definiciones para todos los campos definidos por el usuario en un elemento de Microsoft Outlook y la configuración de enlace de datos para algunos campos integrados.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="ad0ff-106">Se puede manipular mediante programación la estructura de la secuencia de PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ad0ff-107">Sin embargo, puede lograr resultados similares mediante el Diseñador de formularios de Outlook y, en particular, el cuadro de diálogo **Propiedades de** cuadro para un control enlazado a datos.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="ad0ff-108">Las definiciones de campo en una estructura de secuencia PropertyDefinition pueden ser uno de los dos formatos: PropDefV1 y PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ad0ff-109">Outlook admite PropDefV1 y PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ad0ff-110">Todas las definiciones de campo en una estructura de secuencia PropertyDefinition único deben ser del mismo formato.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="ad0ff-111">Para obtener más información acerca de cómo PropDefV1 y PropDefV2 difieren, vea [FieldDefinition secuencia de estructura](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="ad0ff-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="ad0ff-112">Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden especificado a continuación.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="ad0ff-113">Versión: WORD (2 bytes), el formato de las definiciones de campo en el PropertyDefinition en secuencia de estructura.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ad0ff-114">En la siguiente tabla se muestra los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="ad0ff-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ad0ff-115">**Value**</span></span>|<span data-ttu-id="ad0ff-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad0ff-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="ad0ff-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="ad0ff-117">0x0102</span></span>  <br/> |<span data-ttu-id="ad0ff-118">Formato es PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="ad0ff-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="ad0ff-119">0x0103</span></span>  <br/> |<span data-ttu-id="ad0ff-120">Formato es PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="ad0ff-121">FieldDefinitionCount: DWORD (4 bytes), el número de definiciones de campo en esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="ad0ff-122">Éste es el recuento de elementos de matriz en el elemento de datos de FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="ad0ff-123">FieldDefinitions: Una matriz de estructuras de secuencia FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="ad0ff-124">El recuento de esta matriz es igual al elemento de datos de FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="ad0ff-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad0ff-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad0ff-125">See also</span></span>

- [<span data-ttu-id="ad0ff-126">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="ad0ff-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="ad0ff-127">Agregar una definición para un nuevo campo definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="ad0ff-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="ad0ff-128">Ejemplo de flujo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="ad0ff-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="ad0ff-129">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="ad0ff-129">Stream Structures</span></span>](stream-structures.md)

