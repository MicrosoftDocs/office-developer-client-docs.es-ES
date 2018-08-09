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
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816932"
---
# <a name="guid"></a><span data-ttu-id="65f18-103">GUID</span><span class="sxs-lookup"><span data-stu-id="65f18-103">GUID</span></span>

  
  
<span data-ttu-id="65f18-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65f18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65f18-105">Se describe un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="65f18-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65f18-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="65f18-106">Header file:</span></span>  <br/> |<span data-ttu-id="65f18-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="65f18-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="65f18-108">Members</span><span class="sxs-lookup"><span data-stu-id="65f18-108">Members</span></span>

 <span data-ttu-id="65f18-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="65f18-109">**Data1**</span></span>
  
> <span data-ttu-id="65f18-110">Un valor entero largo sin signo de los datos.</span><span class="sxs-lookup"><span data-stu-id="65f18-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="65f18-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="65f18-111">**Data2**</span></span>
  
> <span data-ttu-id="65f18-112">Un valor entero corto sin signo de los datos.</span><span class="sxs-lookup"><span data-stu-id="65f18-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="65f18-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="65f18-113">**Data3**</span></span>
  
> <span data-ttu-id="65f18-114">Un valor entero corto sin signo de los datos.</span><span class="sxs-lookup"><span data-stu-id="65f18-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="65f18-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="65f18-115">**Data4**</span></span>
  
> <span data-ttu-id="65f18-116">Una matriz de caracteres sin firmar.</span><span class="sxs-lookup"><span data-stu-id="65f18-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65f18-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65f18-117">Remarks</span></span>

 <span data-ttu-id="65f18-118">Estructuras **GUID** se usan en MAPI, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="65f18-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="65f18-119">En las estructuras [MAPIUID](mapiuid.md) que identifican los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="65f18-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="65f18-120">Para los identificadores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="65f18-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="65f18-121">En la propiedad establece los nombres de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="65f18-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="65f18-122">Almacén de mensajes y dirección de los proveedores de libreta generan una estructura **GUID** para usar en su estructura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="65f18-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="65f18-123">Al pasar el resultante **MAPIUID** al [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), estos proveedores de servicios de informar a MAPI de su identificador único.</span><span class="sxs-lookup"><span data-stu-id="65f18-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="65f18-124">Además, se usan en la implementación de llamada a procedimiento remoto (RPC) y el lenguaje de descripción de objetos (ODL).</span><span class="sxs-lookup"><span data-stu-id="65f18-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="65f18-125">Para obtener más información acerca de estos usos, vea la *Guía y la referencia del programador de Microsoft RPC*, *referencia del programador de OLE* y *Dentro de OLE*, *Segunda edición* .</span><span class="sxs-lookup"><span data-stu-id="65f18-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="65f18-126">La estructura **GUID** se define en la *referencia del programador de Win32* .</span><span class="sxs-lookup"><span data-stu-id="65f18-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="65f18-127">Los valores específicos para las estructuras **GUID** que se usan dentro de MAPI se definen en el archivo de encabezado Mapiguid.h MAPI.</span><span class="sxs-lookup"><span data-stu-id="65f18-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65f18-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="65f18-128">See also</span></span>



[<span data-ttu-id="65f18-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="65f18-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="65f18-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="65f18-130">MAPI Structures</span></span>](mapi-structures.md)

