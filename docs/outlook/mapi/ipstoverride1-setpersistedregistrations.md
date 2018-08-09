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
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817941"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="c3ef6-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="c3ef6-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="c3ef6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3ef6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3ef6-105">Registra los archivos de carpetas personales (.pst) para el desbloqueo automático, evitar más llamadas a la HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="c3ef6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3ef6-106">Parameters</span></span>

<span data-ttu-id="c3ef6-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="c3ef6-107">_pmval_</span></span>
  
> <span data-ttu-id="c3ef6-108">[entrada] Una estructura [SPropValue](spropvalue.md) que contiene un puntero a la ruta de acceso de la biblioteca de vínculos dinámicos (DLL) para registrar.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="c3ef6-109">La estructura tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="c3ef6-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="c3ef6-110">Un ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="c3ef6-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="c3ef6-111">Una propiedad de valor MVszW que se establece en una matriz de cadenas de caracteres Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="c3ef6-112">Para obtener más información, vea el tema de [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="c3ef6-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c3ef6-113">El SPropValue se almacena en una propiedad MAPI en intervalo interno del PST.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="c3ef6-114">Esta propiedad es inaccesible para las aplicaciones comunes de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="c3ef6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3ef6-115">Return value</span></span>

<span data-ttu-id="c3ef6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3ef6-116">S_OK</span></span> 
  
> <span data-ttu-id="c3ef6-117">La llamada a la función fue correcta.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3ef6-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3ef6-118">Remarks</span></span>

<span data-ttu-id="c3ef6-119">Registros conservados pueden afectar negativamente al rendimiento de aplicaciones, como Outlook y Windows Desktop Search, que abren archivos pst.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="c3ef6-120">Tenga en cuenta el efecto del rendimiento cuando utiliza o expandir el uso de registros conservados.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c3ef6-121">Este método sólo se implementa para Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="c3ef6-122">Además, forma preventiva, se producirá si cualquiera de las rutas de acceso de la matriz no tienen una extensión de nombre de archivo del archivo .dll.</span><span class="sxs-lookup"><span data-stu-id="c3ef6-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3ef6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3ef6-123">See also</span></span>

- [<span data-ttu-id="c3ef6-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3ef6-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="c3ef6-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3ef6-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

