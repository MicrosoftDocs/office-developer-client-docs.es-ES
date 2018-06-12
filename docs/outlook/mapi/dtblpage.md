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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 86cd30b15402f35e8396dedf6b685050ee4fb45e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816756"
---
# <a name="dtblpage"></a><span data-ttu-id="516f2-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="516f2-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="516f2-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="516f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="516f2-105">Describe una página con fichas que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="516f2-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="516f2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="516f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="516f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="516f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="516f2-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="516f2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="516f2-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="516f2-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="516f2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="516f2-110">Members</span></span>

 <span data-ttu-id="516f2-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="516f2-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="516f2-112">Posición en la memoria de la etiqueta de cadena de caracteres de la ficha página.</span><span class="sxs-lookup"><span data-stu-id="516f2-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="516f2-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="516f2-113">**ulFlags**</span></span>
  
> <span data-ttu-id="516f2-114">Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="516f2-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="516f2-115">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="516f2-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="516f2-116">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="516f2-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="516f2-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="516f2-117">The label is in Unicode format.</span></span> <span data-ttu-id="516f2-118">Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="516f2-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="516f2-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="516f2-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="516f2-120">Posición en la memoria de una cadena de caracteres que identifica la sección **[Help File Mappings]** en el archivo MAPISVC. Archivo de configuración de INF o 0.</span><span class="sxs-lookup"><span data-stu-id="516f2-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="516f2-121">El nombre de archivo que aparece en el archivo MAPISVC. Sección INF puede utilizarse por un usuario para tener acceso a información de ayuda sobre la página con fichas haciendo clic en el botón **Ayuda** en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="516f2-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="516f2-122">Para obtener más información acerca de las entradas en MAPISVC. INF, vea [formato de archivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="516f2-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="516f2-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="516f2-123">**ulContext**</span></span>
  
> <span data-ttu-id="516f2-124">Un identificador único para la página con fichas en la cadena definida por el miembro **ulbLpszComponent** .</span><span class="sxs-lookup"><span data-stu-id="516f2-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="516f2-125">El miembro **ulbLpszComponent** y el miembro **ulContext** deben ser distinto de cero para el botón de **Ayuda** para que funcione.</span><span class="sxs-lookup"><span data-stu-id="516f2-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="516f2-126">Si este identificador es cero y la cadena de componente es NULL, no hay ninguna ayuda asociado a la página.</span><span class="sxs-lookup"><span data-stu-id="516f2-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="516f2-127">Notas</span><span class="sxs-lookup"><span data-stu-id="516f2-127">Remarks</span></span>

<span data-ttu-id="516f2-128">Una estructura **DTBLPAGE** describe una página con fichas de un control que se usa para separar varios cuadros de diálogo relacionados.</span><span class="sxs-lookup"><span data-stu-id="516f2-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="516f2-129">Normalmente, estos cuadros de diálogo son hojas de propiedades para mostrar la configuración, mensaje u opciones de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="516f2-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="516f2-130">Al hacer clic en la ficha, el usuario puede cambiar de una hoja a otra.</span><span class="sxs-lookup"><span data-stu-id="516f2-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="516f2-131">El identificador de cadena y el contexto de componente proporcionan información sobre si la Ayuda extendida está disponible para la página con fichas.</span><span class="sxs-lookup"><span data-stu-id="516f2-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="516f2-132">Si la Ayuda extendida está disponible, el identificador de cadena y el contexto de componente proporcionará información acerca de cómo tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="516f2-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="516f2-133">La cadena del componente que se asigna al archivo de ayuda; el identificador de contexto que se asigna al tema de Ayuda inicial.</span><span class="sxs-lookup"><span data-stu-id="516f2-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="516f2-134">Si el identificador de contexto es cero y la cadena de componente es NULL, la información de ayuda no está disponible.</span><span class="sxs-lookup"><span data-stu-id="516f2-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="516f2-135">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="516f2-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="516f2-136">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="516f2-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="516f2-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="516f2-137">See also</span></span>



[<span data-ttu-id="516f2-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="516f2-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="516f2-139">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="516f2-139">MAPI Structures</span></span>](mapi-structures.md)

