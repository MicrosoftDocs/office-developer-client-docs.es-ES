---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408351"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="1e0b2-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="1e0b2-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="1e0b2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e0b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e0b2-105">Registra los archivos de carpetas personales (. pst) para el desbloqueo automático, evitando más llamadas al HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="1e0b2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1e0b2-106">Parameters</span></span>

<span data-ttu-id="1e0b2-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="1e0b2-107">_pmval_</span></span>
  
> <span data-ttu-id="1e0b2-108">a Estructura [SPropValue](spropvalue.md) que contiene un puntero a la ruta de acceso de la biblioteca de vínculos dinámicos (dll) que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="1e0b2-109">La estructura tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="1e0b2-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="1e0b2-110">Un ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="1e0b2-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="1e0b2-111">Una propiedad de valor MVszW que se establece en una matriz de cadenas de caracteres Unicode terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="1e0b2-112">Para obtener más información, vea el tema [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0b2-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1e0b2-113">El SPropValue se almacena en una propiedad MAPI en el intervalo interno del PST.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="1e0b2-114">Esta propiedad es inaccesible para las aplicaciones MAPI ordinarias.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="1e0b2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e0b2-115">Return value</span></span>

<span data-ttu-id="1e0b2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e0b2-116">S_OK</span></span> 
  
> <span data-ttu-id="1e0b2-117">La llamada a la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e0b2-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e0b2-118">Remarks</span></span>

<span data-ttu-id="1e0b2-119">Los registros conservados pueden afectar negativamente al rendimiento de las aplicaciones, como Outlook y la búsqueda en el escritorio de Windows, que abren los archivos PST.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="1e0b2-120">Tenga en cuenta el efecto de rendimiento al usar o ampliar el uso de registros persistentes.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1e0b2-121">Este método se implementa solo para Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="1e0b2-122">Además, se producirá un error anticipadamente si alguna de las rutas de la matriz no tiene una extensión de nombre de archivo. dll.</span><span class="sxs-lookup"><span data-stu-id="1e0b2-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e0b2-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="1e0b2-123">See also</span></span>

- [<span data-ttu-id="1e0b2-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e0b2-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="1e0b2-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e0b2-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

