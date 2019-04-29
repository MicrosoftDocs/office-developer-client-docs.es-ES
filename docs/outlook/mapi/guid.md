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
# <a name="guid"></a><span data-ttu-id="3023f-103">GUID</span><span class="sxs-lookup"><span data-stu-id="3023f-103">GUID</span></span>

  
  
<span data-ttu-id="3023f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3023f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3023f-105">Describe un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="3023f-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3023f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3023f-106">Header file:</span></span>  <br/> |<span data-ttu-id="3023f-107">Mapiguid. h</span><span class="sxs-lookup"><span data-stu-id="3023f-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="3023f-108">Members</span><span class="sxs-lookup"><span data-stu-id="3023f-108">Members</span></span>

 <span data-ttu-id="3023f-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="3023f-109">**Data1**</span></span>
  
> <span data-ttu-id="3023f-110">Valor de datos entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="3023f-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="3023f-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="3023f-111">**Data2**</span></span>
  
> <span data-ttu-id="3023f-112">Valor de datos entero corto sin signo.</span><span class="sxs-lookup"><span data-stu-id="3023f-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="3023f-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="3023f-113">**Data3**</span></span>
  
> <span data-ttu-id="3023f-114">Valor de datos entero corto sin signo.</span><span class="sxs-lookup"><span data-stu-id="3023f-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="3023f-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="3023f-115">**Data4**</span></span>
  
> <span data-ttu-id="3023f-116">Una matriz de caracteres sin signo.</span><span class="sxs-lookup"><span data-stu-id="3023f-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3023f-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3023f-117">Remarks</span></span>

 <span data-ttu-id="3023f-118">Las estructuras **GUID** se usan en MAPI de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3023f-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="3023f-119">En las estructuras [MAPIUID](mapiuid.md) que identifican de forma exclusiva a los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="3023f-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="3023f-120">Para los identificadores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3023f-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="3023f-121">En los nombres de conjunto de propiedades de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="3023f-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="3023f-122">Los proveedores de la libreta de direcciones y el almacén de mensajes generan una estructura **GUID** para usarla en su estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="3023f-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="3023f-123">Al pasar el **MAPIUID** resultante a [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md), estos proveedores de servicios informan a MAPI de su identificador único.</span><span class="sxs-lookup"><span data-stu-id="3023f-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="3023f-124">Además, se usan en la implementación de la llamada a procedimiento remoto (RPC) de Microsoft y el lenguaje de descripción de objetos (ODL).</span><span class="sxs-lookup"><span data-stu-id="3023f-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="3023f-125">Para obtener más información acerca de estos usos, vea la *Guía del programador de Microsoft RPC y referencia*, la *Referencia del programador de OLE* y *en OLE*, *segunda edición* .</span><span class="sxs-lookup"><span data-stu-id="3023f-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="3023f-126">La estructura de **GUID** se define en la *Referencia del programador de Win32* .</span><span class="sxs-lookup"><span data-stu-id="3023f-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="3023f-127">Los valores específicos de las estructuras **GUID** que se usan en MAPI se definen en el archivo de encabezado MAPI Mapiguid. h.</span><span class="sxs-lookup"><span data-stu-id="3023f-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3023f-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="3023f-128">See also</span></span>



[<span data-ttu-id="3023f-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3023f-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="3023f-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="3023f-130">MAPI Structures</span></span>](mapi-structures.md)

