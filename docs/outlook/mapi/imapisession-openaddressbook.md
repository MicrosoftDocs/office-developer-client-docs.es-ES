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
ms.openlocfilehash: 0902aeb71ed66381772a808d21d77edb7e0e2da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589878"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="29168-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="29168-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="29168-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29168-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29168-105">Se abre la libreta de direcciones integrada de MAPI, la devolución de un puntero [IAddrBook](iaddrbookimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="29168-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="29168-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29168-106">Parameters</span></span>

 <span data-ttu-id="29168-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="29168-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="29168-108">[entrada] Un identificador de la ventana primaria del cuadro de diálogo dirección común y otros relacionados con la muestra.</span><span class="sxs-lookup"><span data-stu-id="29168-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="29168-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="29168-109">_lpInterface_</span></span>
  
> <span data-ttu-id="29168-110">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29168-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="29168-111">Si se pasa **null** devuelve un puntero a la interfaz estándar de la libreta de direcciones, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="29168-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="29168-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29168-112">_ulFlags_</span></span>
  
> <span data-ttu-id="29168-113">[entrada] Una máscara de bits de indicadores que controla la apertura de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29168-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="29168-114">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="29168-114">The following flag can be set:</span></span>
    
<span data-ttu-id="29168-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="29168-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="29168-116">Suprime la visualización de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="29168-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="29168-117">Si no está establecido el indicador AB_NO_DIALOG, los proveedores de la libreta de direcciones que contribuyen a la libreta de direcciones integrada pueden pedir al usuario para toda la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="29168-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="29168-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="29168-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="29168-119">[out] Un puntero a un puntero a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29168-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29168-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29168-120">Return value</span></span>

<span data-ttu-id="29168-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="29168-121">S_OK</span></span> 
  
> <span data-ttu-id="29168-122">La libreta de direcciones se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="29168-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="29168-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="29168-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="29168-124">La llamada se ha realizado correctamente, pero no se podrían abrir los contenedores de uno o varios proveedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29168-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="29168-125">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="29168-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="29168-126">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="29168-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="29168-127">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="29168-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29168-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29168-128">Remarks</span></span>

<span data-ttu-id="29168-129">El método **IMAPISession::OpenAddressBook** abre la libreta de direcciones integrada de MAPI, una colección de los contenedores de nivel superior de todos los proveedores de la libreta de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="29168-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="29168-130">El puntero que se devuelve en el parámetro _lppAdrBook_ aún más proporciona acceso al contenido de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29168-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="29168-131">Esto permite que el autor de la llamada realizar tareas como contenedores individuales de apertura, los usuarios de mensajería de buscar y mostrar cuadros de diálogo comunes de dirección.</span><span class="sxs-lookup"><span data-stu-id="29168-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="29168-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="29168-132">Notes to callers</span></span>

 <span data-ttu-id="29168-133">**OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED si no puede cargar uno o varios de los proveedores de la libreta de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="29168-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="29168-134">Este valor es una advertencia, no es un valor de error; controlarla como lo haría S_OK.</span><span class="sxs-lookup"><span data-stu-id="29168-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="29168-135">**OpenAddressBook** siempre devuelve un puntero válido en el parámetro _lppAdrBook_ , independientemente de cómo muchos de los proveedores de la libreta de direcciones no se pudo cargar.</span><span class="sxs-lookup"><span data-stu-id="29168-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="29168-136">Por lo tanto, debe llamar siempre (método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) ) de la libreta de direcciones en algún momento antes de cerrar la sesión.</span><span class="sxs-lookup"><span data-stu-id="29168-136">Therefore, you must always call the address book's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="29168-137">Cuando **OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED, llame a [IMAPISession::GetLastError](imapisession-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contiene información acerca de los proveedores con errores.</span><span class="sxs-lookup"><span data-stu-id="29168-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="29168-138">Se devuelve una única estructura **MAPIERROR** que contiene la información proporcionada por todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="29168-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="29168-139">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="29168-139">MFCMAPI reference</span></span>

<span data-ttu-id="29168-140">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="29168-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="29168-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="29168-141">**File**</span></span>|<span data-ttu-id="29168-142">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="29168-142">**Function**</span></span>|<span data-ttu-id="29168-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="29168-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="29168-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="29168-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="29168-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="29168-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="29168-146">MFCMAPI utiliza el método **IMAPISession::OpenAddressBook** para obtener la libreta de direcciones integrada.</span><span class="sxs-lookup"><span data-stu-id="29168-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29168-147">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="29168-147">See also</span></span>



[<span data-ttu-id="29168-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="29168-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="29168-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="29168-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="29168-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="29168-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="29168-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="29168-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="29168-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="29168-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

