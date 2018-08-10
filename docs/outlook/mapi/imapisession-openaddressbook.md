---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dcde242f5f2e956d1926d6914431008383f5aa55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817440"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="fcbb8-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="fcbb8-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="fcbb8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fcbb8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fcbb8-105">Se abre la libreta de direcciones integrada de MAPI, la devolución de un puntero [IAddrBook](iaddrbookimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="fcbb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcbb8-106">Parameters</span></span>

 <span data-ttu-id="fcbb8-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fcbb8-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="fcbb8-108">[entrada] Un identificador de la ventana primaria del cuadro de diálogo dirección común y otros relacionados con la muestra.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="fcbb8-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fcbb8-109">_lpInterface_</span></span>
  
> <span data-ttu-id="fcbb8-110">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="fcbb8-111">Si se pasa **null** devuelve un puntero a la interfaz estándar de la libreta de direcciones, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fcbb8-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="fcbb8-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fcbb8-112">_ulFlags_</span></span>
  
> <span data-ttu-id="fcbb8-113">[entrada] Una máscara de bits de indicadores que controla la apertura de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="fcbb8-114">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="fcbb8-114">The following flag can be set:</span></span>
    
<span data-ttu-id="fcbb8-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="fcbb8-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="fcbb8-116">Suprime la visualización de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="fcbb8-117">Si no está establecido el indicador AB_NO_DIALOG, los proveedores de la libreta de direcciones que contribuyen a la libreta de direcciones integrada pueden pedir al usuario para toda la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="fcbb8-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="fcbb8-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="fcbb8-119">[out] Un puntero a un puntero a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcbb8-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcbb8-120">Return value</span></span>

<span data-ttu-id="fcbb8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcbb8-121">S_OK</span></span> 
  
> <span data-ttu-id="fcbb8-122">La libreta de direcciones se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="fcbb8-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="fcbb8-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="fcbb8-124">La llamada se ha realizado correctamente, pero no se podrían abrir los contenedores de uno o varios proveedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="fcbb8-125">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="fcbb8-126">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="fcbb8-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="fcbb8-127">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="fcbb8-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcbb8-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcbb8-128">Remarks</span></span>

<span data-ttu-id="fcbb8-129">El método **IMAPISession::OpenAddressBook** abre la libreta de direcciones integrada de MAPI, una colección de los contenedores de nivel superior de todos los proveedores de la libreta de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="fcbb8-130">El puntero que se devuelve en el parámetro _lppAdrBook_ aún más proporciona acceso al contenido de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="fcbb8-131">Esto permite que el autor de la llamada realizar tareas como contenedores individuales de apertura, los usuarios de mensajería de buscar y mostrar cuadros de diálogo comunes de dirección.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fcbb8-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="fcbb8-132">Notes to callers</span></span>

 <span data-ttu-id="fcbb8-133">**OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED si no puede cargar uno o varios de los proveedores de la libreta de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="fcbb8-134">Este valor es una advertencia, no es un valor de error; controlarla como lo haría S_OK.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="fcbb8-135">**OpenAddressBook** siempre devuelve un puntero válido en el parámetro _lppAdrBook_ , independientemente de cómo muchos de los proveedores de la libreta de direcciones no se pudo cargar.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="fcbb8-136">Por lo tanto, debe llamar siempre (método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) ) de la libreta de direcciones en algún momento antes de cerrar la sesión.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-136">Therefore, you must always call the address book's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="fcbb8-137">Cuando **OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED, llame a [IMAPISession::GetLastError](imapisession-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contiene información acerca de los proveedores con errores.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="fcbb8-138">Se devuelve una única estructura **MAPIERROR** que contiene la información proporcionada por todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fcbb8-139">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fcbb8-139">MFCMAPI reference</span></span>

<span data-ttu-id="fcbb8-140">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fcbb8-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="fcbb8-141">**File**</span></span>|<span data-ttu-id="fcbb8-142">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="fcbb8-142">**Function**</span></span>|<span data-ttu-id="fcbb8-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="fcbb8-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcbb8-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="fcbb8-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="fcbb8-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="fcbb8-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="fcbb8-146">MFCMAPI utiliza el método **IMAPISession::OpenAddressBook** para obtener la libreta de direcciones integrada.</span><span class="sxs-lookup"><span data-stu-id="fcbb8-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcbb8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcbb8-147">See also</span></span>



[<span data-ttu-id="fcbb8-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fcbb8-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="fcbb8-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fcbb8-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="fcbb8-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="fcbb8-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="fcbb8-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcbb8-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="fcbb8-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="fcbb8-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

