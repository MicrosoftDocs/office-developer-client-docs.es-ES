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
ms.openlocfilehash: 769ae984e4b6e8610ca7909ea2ac714d9d04d698
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589675"
---
# <a name="dtpage"></a><span data-ttu-id="742b6-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="742b6-103">DTPAGE</span></span>

  
  
<span data-ttu-id="742b6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="742b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="742b6-105">Describe el cuadro de diálogo que se genera a partir de una tabla para mostrar por la función [BuildDisplayTable](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="742b6-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="742b6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="742b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="742b6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="742b6-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="742b6-108">Members</span><span class="sxs-lookup"><span data-stu-id="742b6-108">Members</span></span>

 <span data-ttu-id="742b6-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="742b6-109">**cctl**</span></span>
  
> <span data-ttu-id="742b6-110">Recuento de controles que señala el miembro **lpctl** .</span><span class="sxs-lookup"><span data-stu-id="742b6-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="742b6-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="742b6-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="742b6-112">Puntero al nombre o número entero identificador para el recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="742b6-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="742b6-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="742b6-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="742b6-114">Puntero a la cadena que aparece en la sección **[Help File Mappings]** en MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="742b6-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="742b6-115">Debido a que **lpszComponent** se encuentra en una unión con el miembro **ulItemID** , solo uno de estos miembros tiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="742b6-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="742b6-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="742b6-116">**ulItemID**</span></span>
  
> <span data-ttu-id="742b6-117">Identificador de recurso de entero con un valor menor o igual que 65535 desde la que se puede leer el nombre de archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="742b6-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="742b6-118">Debido a que **ulItemID** se encuentra en una unión con el miembro **lpszComponent** , solo uno de estos miembros tiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="742b6-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="742b6-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="742b6-119">**lpctl**</span></span>
  
> <span data-ttu-id="742b6-120">Puntero a una matriz de estructuras [DTCTL](dtctl.md) , uno para cada control en la página.</span><span class="sxs-lookup"><span data-stu-id="742b6-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="742b6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="742b6-121">Remarks</span></span>

<span data-ttu-id="742b6-122">Para identificar el archivo de ayuda para la página con fichas, establezca el miembro **lpszComponent** en una cadena codificado de forma rígida o el miembro **ulItemID** en un identificador de recurso de entero.</span><span class="sxs-lookup"><span data-stu-id="742b6-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="742b6-123">Cada entrada en la sección **[Help File Mappings]** en MAPISVC. INF consta de una cadena de componente, no más de 30 caracteres, en el lado izquierdo y una ruta de acceso del archivo de Ayuda de la derecha.</span><span class="sxs-lookup"><span data-stu-id="742b6-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="742b6-124">**UlItemID** y **lpszResourceName** se encuentran en el parámetro _hInstance_ del **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="742b6-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="742b6-125">Para obtener más información, vea [MAPISVC. INF [asignaciones de archivo de ayuda] sección](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="742b6-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="742b6-126">Aunque **BuildDisplayTable** usa esta estructura para crear la tabla para mostrar de los recursos de control, la estructura **DTPAGE** nunca aparece en la propia tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="742b6-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="742b6-127">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="742b6-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="742b6-128">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="742b6-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="742b6-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="742b6-129">See also</span></span>



[<span data-ttu-id="742b6-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="742b6-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="742b6-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="742b6-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="742b6-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="742b6-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="742b6-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="742b6-133">MAPI Structures</span></span>](mapi-structures.md)

