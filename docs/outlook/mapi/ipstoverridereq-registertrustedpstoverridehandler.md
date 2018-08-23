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
ms.openlocfilehash: 62269b823810964fc0e5749aa6a57d39c503e2b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573582"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="86154-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="86154-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="86154-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86154-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86154-105">Inicia el procedimiento de desbloqueo para un archivo de carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="86154-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="86154-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86154-106">Parameters</span></span>

 <span data-ttu-id="86154-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="86154-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="86154-108">[entrada] Un puntero a la ruta de acceso de una biblioteca de vínculos dinámicos (DLL) de otro fabricante.</span><span class="sxs-lookup"><span data-stu-id="86154-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="86154-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="86154-109">_pvClientData_</span></span>
  
> <span data-ttu-id="86154-110">[entrada] Un puntero a datos de cliente, que se pasa por el proveedor de PST en llamadas posteriores a la función de archivo DLL HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="86154-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="86154-111">Estos datos de cliente pueden usar el archivo DLL para ayudarle a comprobar si se debe desbloquear el archivo PST.</span><span class="sxs-lookup"><span data-stu-id="86154-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86154-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86154-112">Return value</span></span>

<span data-ttu-id="86154-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="86154-113">S_OK</span></span>
  
> <span data-ttu-id="86154-114">La llamada a la función fue correcta.</span><span class="sxs-lookup"><span data-stu-id="86154-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86154-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86154-115">Remarks</span></span>

<span data-ttu-id="86154-116">El archivo DLL especificado por el parámetro wzDllPath debe haber iniciado sesión con un certificado digital.</span><span class="sxs-lookup"><span data-stu-id="86154-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="86154-117">El archivo DLL también debe exportar una función con la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="86154-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="86154-118">Esta función se llamará con un puntero al objeto IMsgStore para los archivos PST, un puntero a un objeto IUnknown que implementa la interfaz IPSTOVERRIDE1 y un puntero a los datos proporcionados originalmente a través de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="86154-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="86154-119">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="86154-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86154-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86154-120">See also</span></span>



[<span data-ttu-id="86154-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86154-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="86154-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86154-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

