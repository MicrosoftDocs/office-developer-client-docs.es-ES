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
# <a name="dtpage"></a><span data-ttu-id="d647f-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="d647f-103">DTPAGE</span></span>

  
  
<span data-ttu-id="d647f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d647f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d647f-105">Describe el cuadro de diálogo creado a partir de una tabla para mostrar mediante la [función BuildDisplayTable.](builddisplaytable.md)</span><span class="sxs-lookup"><span data-stu-id="d647f-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d647f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d647f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d647f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d647f-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d647f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d647f-108">Members</span></span>

 <span data-ttu-id="d647f-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="d647f-109">**cctl**</span></span>
  
> <span data-ttu-id="d647f-110">Recuento de controles a los que apunta el **miembro lpctl.**</span><span class="sxs-lookup"><span data-stu-id="d647f-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="d647f-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="d647f-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="d647f-112">Puntero al nombre o al identificador entero del recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d647f-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="d647f-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="d647f-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="d647f-114">Puntero a la cadena que aparece en la **sección [Asignaciones** de archivos de Ayuda] en MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="d647f-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="d647f-115">Dado **que lpszComponent** está en una unión con el **miembro ulItemID,** solo uno de estos miembros tiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="d647f-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="d647f-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="d647f-116">**ulItemID**</span></span>
  
> <span data-ttu-id="d647f-117">Identificador de recurso entero con un valor menor o igual que 65535 desde el que se puede leer el nombre del archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="d647f-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="d647f-118">Dado **que ulItemID** está en una unión con el **miembro lpszComponent,** solo uno de estos miembros tiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="d647f-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="d647f-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="d647f-119">**lpctl**</span></span>
  
> <span data-ttu-id="d647f-120">Puntero a una matriz [de estructuras DTCTL,](dtctl.md) una para cada control de la página.</span><span class="sxs-lookup"><span data-stu-id="d647f-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d647f-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d647f-121">Remarks</span></span>

<span data-ttu-id="d647f-122">Para identificar el archivo de Ayuda de la página con fichas, establezca el miembro **lpszComponent** en una cadena codificada de forma fija o el miembro **ulItemID** en un identificador de recurso entero.</span><span class="sxs-lookup"><span data-stu-id="d647f-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="d647f-123">Cada entrada de la **sección [Asignaciones de** archivos de ayuda] en MAPISVC. INF consta de una cadena de componente, que no tiene más de 30 caracteres, en el lado izquierdo y una ruta de acceso del archivo de Ayuda a la derecha.</span><span class="sxs-lookup"><span data-stu-id="d647f-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="d647f-124">Tanto **ulItemID** como **lpszResourceName** se encuentran en el parámetro  _hInstance_ de **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="d647f-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="d647f-125">Para obtener más información, vea [MAPISVC. INF [Asignaciones de archivo de ayuda] Sección](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="d647f-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="d647f-126">Aunque **BuildDisplayTable** usa esta estructura para crear la tabla para mostrar a partir de recursos de control, la estructura **DTPAGE** nunca aparece en la propia tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="d647f-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="d647f-127">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="d647f-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="d647f-128">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="d647f-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d647f-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d647f-129">See also</span></span>



[<span data-ttu-id="d647f-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="d647f-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="d647f-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="d647f-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="d647f-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="d647f-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="d647f-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d647f-133">MAPI Structures</span></span>](mapi-structures.md)

