---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340120"
---
# <a name="dtblpage"></a><span data-ttu-id="f0464-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="f0464-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="f0464-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0464-105">Describe una página con fichas que se utilizará en un cuadro de diálogo que se genera a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="f0464-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0464-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f0464-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0464-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f0464-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f0464-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="f0464-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f0464-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="f0464-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="f0464-110">Members</span><span class="sxs-lookup"><span data-stu-id="f0464-110">Members</span></span>

 <span data-ttu-id="f0464-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="f0464-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="f0464-112">Posición en la memoria de la etiqueta de la cadena de caracteres para la ficha de página.</span><span class="sxs-lookup"><span data-stu-id="f0464-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="f0464-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f0464-113">**ulFlags**</span></span>
  
> <span data-ttu-id="f0464-114">Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="f0464-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="f0464-115">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="f0464-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="f0464-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0464-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f0464-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0464-117">The label is in Unicode format.</span></span> <span data-ttu-id="f0464-118">Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0464-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="f0464-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="f0464-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="f0464-120">Posición en la memoria de una cadena de caracteres que identifica la sección **[asignaciones de archivos de ayuda] del archivo** MAPISVC. Archivo de configuración INF o 0.</span><span class="sxs-lookup"><span data-stu-id="f0464-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="f0464-121">Nombre de archivo que aparece en el archivo MAPISVC. INF puede ser usada por un usuario para tener acceso a la ayuda ampliada de la página con fichas haciendo clic en el botón **ayuda** en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f0464-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="f0464-122">Para obtener más información acerca de las entradas de MAPISVC. INF, vea el [formato de archivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="f0464-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="f0464-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="f0464-123">**ulContext**</span></span>
  
> <span data-ttu-id="f0464-124">Un identificador único para la página con fichas en la cadena definida por el miembro **ulbLpszComponent** .</span><span class="sxs-lookup"><span data-stu-id="f0464-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="f0464-125">El miembro **ulbLpszComponent** y el miembro **ulContext** deben ser distintos de cero para que funcione el botón **ayuda** .</span><span class="sxs-lookup"><span data-stu-id="f0464-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="f0464-126">Si este identificador es cero y la cadena del componente es NULL, no hay ayuda asociada a la página.</span><span class="sxs-lookup"><span data-stu-id="f0464-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f0464-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0464-127">Remarks</span></span>

<span data-ttu-id="f0464-128">Una estructura **DTBLPAGE** describe una página con fichas un control que se usa para separar varios cuadros de diálogo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f0464-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="f0464-129">Normalmente, estos cuadros de diálogo son hojas de propiedades para mostrar opciones de configuración, mensajes o destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f0464-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="f0464-130">Al hacer clic en la pestaña, el usuario puede cambiar de una hoja a otra.</span><span class="sxs-lookup"><span data-stu-id="f0464-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="f0464-131">El identificador de contexto y la cadena de componentes proporcionan información sobre si la ayuda ampliada está disponible para la página con fichas.</span><span class="sxs-lookup"><span data-stu-id="f0464-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="f0464-132">Si hay disponible ayuda ampliada, el identificador de contexto y la cadena de componentes proporcionarán información sobre cómo obtener acceso a ella.</span><span class="sxs-lookup"><span data-stu-id="f0464-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="f0464-133">La cadena de componente se asigna al archivo de ayuda; el identificador de contexto se asigna al tema de ayuda inicial.</span><span class="sxs-lookup"><span data-stu-id="f0464-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="f0464-134">Si el identificador de contexto es cero y la cadena del componente es NULL, la ayuda extendida no está disponible.</span><span class="sxs-lookup"><span data-stu-id="f0464-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="f0464-135">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f0464-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f0464-136">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f0464-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0464-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0464-137">See also</span></span>



[<span data-ttu-id="f0464-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f0464-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="f0464-139">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f0464-139">MAPI Structures</span></span>](mapi-structures.md)

