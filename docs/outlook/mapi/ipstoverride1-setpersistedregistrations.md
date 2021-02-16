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
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="f4a68-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="f4a68-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="f4a68-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4a68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4a68-105">Registra archivos de carpetas personales (.pst) para el desbloqueo automático, evitando llamadas adicionales a HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="f4a68-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="f4a68-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4a68-106">Parameters</span></span>

<span data-ttu-id="f4a68-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="f4a68-107">_pmval_</span></span>
  
> <span data-ttu-id="f4a68-108">[entrada] Estructura [SPropValue](spropvalue.md) que contiene un puntero a la ruta de acceso de la biblioteca de vínculos dinámicos (DLL) que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="f4a68-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="f4a68-109">La estructura tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="f4a68-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="f4a68-110">Una ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f4a68-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="f4a68-111">Una propiedad de valor MVszW que se establece en una matriz de cadenas de caracteres Unicode terminadas en null.</span><span class="sxs-lookup"><span data-stu-id="f4a68-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="f4a68-112">Para obtener más información, consulte [el tema SWStringArray.](swstringarray.md)</span><span class="sxs-lookup"><span data-stu-id="f4a68-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f4a68-113">SPropValue se almacena en una propiedad MAPI en el intervalo interno de PST.</span><span class="sxs-lookup"><span data-stu-id="f4a68-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="f4a68-114">Esta propiedad no es accesible para las aplicaciones MAPI normales.</span><span class="sxs-lookup"><span data-stu-id="f4a68-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="f4a68-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4a68-115">Return value</span></span>

<span data-ttu-id="f4a68-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4a68-116">S_OK</span></span> 
  
> <span data-ttu-id="f4a68-117">La llamada a la función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4a68-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4a68-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4a68-118">Remarks</span></span>

<span data-ttu-id="f4a68-119">Los registros persistentes pueden afectar negativamente al rendimiento de las aplicaciones, como Outlook y Windows Desktop Search, que abren archivos PST.</span><span class="sxs-lookup"><span data-stu-id="f4a68-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="f4a68-120">Tenga en cuenta el efecto de rendimiento al usar o ampliar el uso de registros persistentes.</span><span class="sxs-lookup"><span data-stu-id="f4a68-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f4a68-121">Este método se implementa solo para Unicode.</span><span class="sxs-lookup"><span data-stu-id="f4a68-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="f4a68-122">Además, se producirá un error preferentemente si alguna de las rutas de acceso de la matriz no tiene una extensión de nombre de archivo de .dll.</span><span class="sxs-lookup"><span data-stu-id="f4a68-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4a68-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4a68-123">See also</span></span>

- [<span data-ttu-id="f4a68-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4a68-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="f4a68-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4a68-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

