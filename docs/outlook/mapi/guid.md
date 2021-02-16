---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421588"
---
# <a name="guid"></a><span data-ttu-id="f7f11-103">GUID</span><span class="sxs-lookup"><span data-stu-id="f7f11-103">GUID</span></span>

  
  
<span data-ttu-id="f7f11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7f11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7f11-105">Describe un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="f7f11-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7f11-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f7f11-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7f11-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="f7f11-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="f7f11-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7f11-108">Members</span></span>

 <span data-ttu-id="f7f11-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="f7f11-109">**Data1**</span></span>
  
> <span data-ttu-id="f7f11-110">Un valor de datos enteros largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="f7f11-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="f7f11-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="f7f11-111">**Data2**</span></span>
  
> <span data-ttu-id="f7f11-112">Un valor de datos enteros cortos sin signo.</span><span class="sxs-lookup"><span data-stu-id="f7f11-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="f7f11-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="f7f11-113">**Data3**</span></span>
  
> <span data-ttu-id="f7f11-114">Un valor de datos enteros cortos sin signo.</span><span class="sxs-lookup"><span data-stu-id="f7f11-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="f7f11-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="f7f11-115">**Data4**</span></span>
  
> <span data-ttu-id="f7f11-116">Matriz de caracteres sin signo.</span><span class="sxs-lookup"><span data-stu-id="f7f11-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7f11-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7f11-117">Remarks</span></span>

 <span data-ttu-id="f7f11-118">**Las** estructuras GUID se usan en MAPI de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f7f11-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="f7f11-119">En las [estructuras MAPIUID](mapiuid.md) que identifican de forma única los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="f7f11-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="f7f11-120">Para identificadores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="f7f11-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="f7f11-121">En el conjunto de propiedades nombres de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="f7f11-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="f7f11-122">Los proveedores de almacén de mensajes y libreta de direcciones generan **una estructura GUID** para usarla en su estructura **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="f7f11-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="f7f11-123">Al pasar el **MAPIUID resultante** a [IMAPISupport::SetProviderUID,](imapisupport-setprovideruid.md)estos proveedores de servicios informan a MAPI de su identificador único.</span><span class="sxs-lookup"><span data-stu-id="f7f11-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="f7f11-124">Además, se usan en la implementación de Microsoft Remote Procedure Call (RPC) y el Lenguaje de descripción de objetos (ODL).</span><span class="sxs-lookup"><span data-stu-id="f7f11-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="f7f11-125">Para obtener más información acerca de estos usos, vea la guía y la referencia del programador de RPC de *Microsoft,* la referencia del programador *OLE* y *Inside OLE*, segunda *edición.*</span><span class="sxs-lookup"><span data-stu-id="f7f11-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="f7f11-126">La **estructura GUID** se define en la referencia del programador de *Win32.*</span><span class="sxs-lookup"><span data-stu-id="f7f11-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="f7f11-127">Los valores específicos **de las** estructuras GUID que se usan dentro de MAPI se definen en el archivo de encabezado MAPI Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="f7f11-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7f11-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7f11-128">See also</span></span>



[<span data-ttu-id="f7f11-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f7f11-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="f7f11-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f7f11-130">MAPI Structures</span></span>](mapi-structures.md)

