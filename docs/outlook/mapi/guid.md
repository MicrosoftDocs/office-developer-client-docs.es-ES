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
ms.openlocfilehash: 94bafdf0ca84fa31a7df2f022265d5d5d1a99a37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577698"
---
# <a name="guid"></a><span data-ttu-id="e6855-103">GUID</span><span class="sxs-lookup"><span data-stu-id="e6855-103">GUID</span></span>

  
  
<span data-ttu-id="e6855-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6855-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6855-105">Se describe un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="e6855-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6855-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e6855-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6855-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="e6855-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="e6855-108">Members</span><span class="sxs-lookup"><span data-stu-id="e6855-108">Members</span></span>

 <span data-ttu-id="e6855-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="e6855-109">**Data1**</span></span>
  
> <span data-ttu-id="e6855-110">Un valor entero largo sin signo de los datos.</span><span class="sxs-lookup"><span data-stu-id="e6855-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="e6855-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="e6855-111">**Data2**</span></span>
  
> <span data-ttu-id="e6855-112">Un valor entero corto sin signo de los datos.</span><span class="sxs-lookup"><span data-stu-id="e6855-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="e6855-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="e6855-113">**Data3**</span></span>
  
> <span data-ttu-id="e6855-114">Un valor entero corto sin signo de los datos.</span><span class="sxs-lookup"><span data-stu-id="e6855-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="e6855-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="e6855-115">**Data4**</span></span>
  
> <span data-ttu-id="e6855-116">Una matriz de caracteres sin firmar.</span><span class="sxs-lookup"><span data-stu-id="e6855-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6855-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6855-117">Remarks</span></span>

 <span data-ttu-id="e6855-118">Estructuras **GUID** se usan en MAPI, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e6855-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="e6855-119">En las estructuras [MAPIUID](mapiuid.md) que identifican los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="e6855-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="e6855-120">Para los identificadores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="e6855-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="e6855-121">En la propiedad establece los nombres de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="e6855-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="e6855-122">Almacén de mensajes y dirección de los proveedores de libreta generan una estructura **GUID** para usar en su estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="e6855-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="e6855-123">Al pasar el resultante **MAPIUID** al [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), estos proveedores de servicios de informar a MAPI de su identificador único.</span><span class="sxs-lookup"><span data-stu-id="e6855-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="e6855-124">Además, se usan en la implementación de llamada a procedimiento remoto (RPC) y el lenguaje de descripción de objetos (ODL).</span><span class="sxs-lookup"><span data-stu-id="e6855-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="e6855-125">Para obtener más información acerca de estos usos, vea la *Guía y la referencia del programador de Microsoft RPC*, *referencia del programador de OLE* y *Dentro de OLE*, *Segunda edición* .</span><span class="sxs-lookup"><span data-stu-id="e6855-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="e6855-126">La estructura **GUID** se define en la *referencia del programador de Win32* .</span><span class="sxs-lookup"><span data-stu-id="e6855-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="e6855-127">Los valores específicos para las estructuras **GUID** que se usan dentro de MAPI se definen en el archivo de encabezado Mapiguid.h MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6855-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6855-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e6855-128">See also</span></span>



[<span data-ttu-id="e6855-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e6855-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="e6855-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e6855-130">MAPI Structures</span></span>](mapi-structures.md)

