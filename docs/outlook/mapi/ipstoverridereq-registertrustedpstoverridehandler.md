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
description: 'Última modificación: 24 de febrero de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279538"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="793b4-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="793b4-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="793b4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="793b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="793b4-105">Inicia el proceso de desbloqueo de un archivo de carpetas personales (. pst).</span><span class="sxs-lookup"><span data-stu-id="793b4-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="793b4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="793b4-106">Parameters</span></span>

 <span data-ttu-id="793b4-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="793b4-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="793b4-108">a Un puntero a la ruta de acceso de una biblioteca de vínculos dinámicos (DLL) de terceros.</span><span class="sxs-lookup"><span data-stu-id="793b4-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="793b4-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="793b4-109">_pvClientData_</span></span>
  
> <span data-ttu-id="793b4-110">a Un puntero a datos de cliente, que el proveedor PST pasará a las llamadas posteriores a la función HrTrustedPSTOverrideHandlerCallback del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="793b4-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="793b4-111">El DLL puede usar estos datos del cliente para ayudar a comprobar si el archivo PST debe estar desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="793b4-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="793b4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="793b4-112">Return value</span></span>

<span data-ttu-id="793b4-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="793b4-113">S_OK</span></span>
  
> <span data-ttu-id="793b4-114">La llamada a la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="793b4-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="793b4-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="793b4-115">Remarks</span></span>

<span data-ttu-id="793b4-116">La DLL especificada por el parámetro wzDllPath debe estar firmada con un certificado digital.</span><span class="sxs-lookup"><span data-stu-id="793b4-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="793b4-117">La DLL también debe exportar una función con la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="793b4-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="793b4-118">Se llama a esta función con un puntero al objeto IMsgStore para el archivo PST, un puntero a un objeto IUnknown que implementa la interfaz IPSTOVERRIDE1 y un puntero a los datos proporcionados originalmente a través de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="793b4-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="793b4-119">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para omitir la Directiva PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="793b4-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="793b4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="793b4-120">See also</span></span>



[<span data-ttu-id="793b4-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="793b4-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="793b4-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="793b4-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

