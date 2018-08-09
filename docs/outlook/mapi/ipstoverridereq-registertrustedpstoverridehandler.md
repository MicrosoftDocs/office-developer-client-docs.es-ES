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
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817940"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="1f7a8-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="1f7a8-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="1f7a8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f7a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f7a8-105">Inicia el procedimiento de desbloqueo para un archivo de carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="1f7a8-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="1f7a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f7a8-106">Parameters</span></span>

 <span data-ttu-id="1f7a8-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="1f7a8-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="1f7a8-108">[entrada] Un puntero a la ruta de acceso de una biblioteca de vínculos dinámicos (DLL) de otro fabricante.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="1f7a8-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="1f7a8-109">_pvClientData_</span></span>
  
> <span data-ttu-id="1f7a8-110">[entrada] Un puntero a datos de cliente, que se pasa por el proveedor de PST en llamadas posteriores a la función de archivo DLL HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="1f7a8-111">Estos datos de cliente pueden usar el archivo DLL para ayudarle a comprobar si se debe desbloquear el archivo PST.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f7a8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f7a8-112">Return value</span></span>

<span data-ttu-id="1f7a8-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f7a8-113">S_OK</span></span>
  
> <span data-ttu-id="1f7a8-114">La llamada a la función fue correcta.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f7a8-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f7a8-115">Remarks</span></span>

<span data-ttu-id="1f7a8-116">El archivo DLL especificado por el parámetro wzDllPath debe haber iniciado sesión con un certificado digital.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="1f7a8-117">El archivo DLL también debe exportar una función con la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="1f7a8-118">Esta función se llamará con un puntero al objeto IMsgStore para los archivos PST, un puntero a un objeto IUnknown que implementa la interfaz IPSTOVERRIDE1 y un puntero a los datos proporcionados originalmente a través de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="1f7a8-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="1f7a8-119">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="1f7a8-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f7a8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f7a8-120">See also</span></span>



[<span data-ttu-id="1f7a8-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f7a8-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="1f7a8-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f7a8-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

