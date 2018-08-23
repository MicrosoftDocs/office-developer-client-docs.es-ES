---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f01d0ad7e7e6b1ad7a5e4c4838bb46ca143e0968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567058"
---
# <a name="checkparameters"></a><span data-ttu-id="ce85a-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="ce85a-103">CheckParameters</span></span>

  
  
<span data-ttu-id="ce85a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce85a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce85a-105">Llama a una función interna para validar parámetros de depuración en los métodos de proveedor de servicio llamados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce85a-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce85a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ce85a-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce85a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ce85a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ce85a-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ce85a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce85a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce85a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce85a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ce85a-110">Called by:</span></span>  <br/> |<span data-ttu-id="ce85a-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ce85a-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="ce85a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce85a-112">Parameters</span></span>

 <span data-ttu-id="ce85a-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="ce85a-113">_eMethod_</span></span>
  
> <span data-ttu-id="ce85a-114">[entrada] Especifica el (enumeración), el método para validar.</span><span class="sxs-lookup"><span data-stu-id="ce85a-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="ce85a-115">_Primero_</span><span class="sxs-lookup"><span data-stu-id="ce85a-115">_First_</span></span>
  
> <span data-ttu-id="ce85a-116">[entrada] Puntero al primer argumento en la pila.</span><span class="sxs-lookup"><span data-stu-id="ce85a-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce85a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce85a-117">Return value</span></span>

<span data-ttu-id="ce85a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce85a-118">S_OK</span></span> 
  
> <span data-ttu-id="ce85a-119">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="ce85a-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce85a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce85a-120">Remarks</span></span>

<span data-ttu-id="ce85a-121">La macro **CheckParameters** se ha sustituido por la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="ce85a-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="ce85a-122">Se recomienda **CheckParms** en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="ce85a-122">**CheckParms** is recommended on all platforms.</span></span> 
  

