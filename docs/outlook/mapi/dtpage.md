---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408225"
---
# <a name="dtpage"></a><span data-ttu-id="ad474-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="ad474-103">DTPAGE</span></span>

  
  
<span data-ttu-id="ad474-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad474-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad474-105">Describe el cuadro de diálogo que se genera a partir de una tabla de presentación por la función [BuildDisplayTable](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="ad474-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad474-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ad474-106">Header file:</span></span>  <br/> |<span data-ttu-id="ad474-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ad474-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a><span data-ttu-id="ad474-108">Members</span><span class="sxs-lookup"><span data-stu-id="ad474-108">Members</span></span>

 <span data-ttu-id="ad474-109">**CCTL**</span><span class="sxs-lookup"><span data-stu-id="ad474-109">**cctl**</span></span>
  
> <span data-ttu-id="ad474-110">Número de controles a los que apunta el miembro **lpctl** .</span><span class="sxs-lookup"><span data-stu-id="ad474-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="ad474-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="ad474-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="ad474-112">Puntero al nombre o al identificador entero del recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ad474-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="ad474-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="ad474-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="ad474-114">Puntero a la cadena que aparece en la sección **[file mappings de la ayuda]** en MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="ad474-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="ad474-115">Como **lpszComponent** está en una unión con el miembro **ulItemID** , solo uno de estos miembros tiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="ad474-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="ad474-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="ad474-116">**ulItemID**</span></span>
  
> <span data-ttu-id="ad474-117">Identificador de recursos entero con un valor inferior o igual a 65535 desde el que se puede leer el nombre del archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="ad474-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="ad474-118">Como **ulItemID** está en una unión con el miembro **lpszComponent** , solo uno de estos miembros tiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="ad474-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="ad474-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="ad474-119">**lpctl**</span></span>
  
> <span data-ttu-id="ad474-120">Puntero a una matriz de estructuras [DTCTL](dtctl.md) , una para cada control de la página.</span><span class="sxs-lookup"><span data-stu-id="ad474-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ad474-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad474-121">Remarks</span></span>

<span data-ttu-id="ad474-122">Para identificar el archivo de ayuda de la página con fichas, establezca el miembro **lpszComponent** en una cadena codificada de forma rígida, o bien el miembro **ulItemID** en un identificador de recursos entero.</span><span class="sxs-lookup"><span data-stu-id="ad474-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="ad474-123">Cada entrada de la sección **[file mappings de la ayuda]** de MAPISVC. INF consta de una cadena de componente, de no más de 30 caracteres, en el lado izquierdo y de una ruta de acceso del archivo de ayuda a la derecha.</span><span class="sxs-lookup"><span data-stu-id="ad474-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="ad474-124">Tanto **ulItemID** como **lpszResourceName** se encuentran en el parámetro _hInstance_ de **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="ad474-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="ad474-125">Para obtener más información, vea [MAPISVC. Sección INF [asignaciones de archivos de ayuda]](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="ad474-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="ad474-126">Aunque **BuildDisplayTable** usa esta estructura para compilar la tabla de presentación a partir de los recursos de control, la estructura **DTPAGE** nunca aparece en la propia tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="ad474-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="ad474-127">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ad474-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ad474-128">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="ad474-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad474-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="ad474-129">See also</span></span>



[<span data-ttu-id="ad474-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="ad474-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="ad474-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="ad474-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="ad474-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ad474-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="ad474-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="ad474-133">MAPI Structures</span></span>](mapi-structures.md)

