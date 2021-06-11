---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Last modified: February 24, 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279538"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="4c0ef-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="4c0ef-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="4c0ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c0ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c0ef-105">Inicia el procedimiento de desbloqueo de un archivo carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="4c0ef-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="4c0ef-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4c0ef-106">Parameters</span></span>

 <span data-ttu-id="4c0ef-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="4c0ef-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="4c0ef-108">[in] Puntero a la ruta de acceso de una biblioteca de vínculos dinámicos (DLL) de terceros.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="4c0ef-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="4c0ef-109">_pvClientData_</span></span>
  
> <span data-ttu-id="4c0ef-110">[in] Un puntero a los datos de cliente, que pasará el proveedor pst en llamadas posteriores a la función HrTrustedPSTOverrideHandlerCallback del DLL.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="4c0ef-111">La DLL puede usar estos datos de cliente para ayudar a comprobar si el PST debe desbloquearse.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c0ef-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c0ef-112">Return value</span></span>

<span data-ttu-id="4c0ef-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c0ef-113">S_OK</span></span>
  
> <span data-ttu-id="4c0ef-114">La llamada a la función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c0ef-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c0ef-115">Remarks</span></span>

<span data-ttu-id="4c0ef-116">La DLL especificada por el parámetro wzDllPath debe firmarse con un certificado digital.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="4c0ef-117">La DLL también debe exportar una función con la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="4c0ef-118">Se llamará a esta función con un puntero al objeto IMsgStore del PST, un puntero a un objeto IUnknown que implementa la interfaz IPSTOVERRIDE1 y un puntero a los datos proporcionados originalmente a través de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="4c0ef-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="4c0ef-119">Para obtener más información, vea [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="4c0ef-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c0ef-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c0ef-120">See also</span></span>



[<span data-ttu-id="4c0ef-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c0ef-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="4c0ef-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c0ef-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

