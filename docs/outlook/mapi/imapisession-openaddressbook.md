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
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329424"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="a82ae-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="a82ae-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="a82ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a82ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a82ae-105">Abre la libreta de direcciones integrada mapi y devuelve un [puntero IAddrBook](iaddrbookimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="a82ae-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="a82ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a82ae-106">Parameters</span></span>

 <span data-ttu-id="a82ae-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a82ae-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a82ae-108">[entrada] Identificador de la ventana principal del cuadro de diálogo de dirección común y otras pantallas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a82ae-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="a82ae-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a82ae-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a82ae-110">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a82ae-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="a82ae-111">Pasar **null** devuelve un puntero a la interfaz estándar de la libreta de direcciones, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="a82ae-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="a82ae-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a82ae-112">_ulFlags_</span></span>
  
> <span data-ttu-id="a82ae-113">[entrada] Máscara de bits de marcas que controla la apertura de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a82ae-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="a82ae-114">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a82ae-114">The following flag can be set:</span></span>
    
<span data-ttu-id="a82ae-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a82ae-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="a82ae-116">Suprime la presentación de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a82ae-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="a82ae-117">Si no AB_NO_DIALOG marca, los proveedores de libretas de direcciones que contribuyen a la libreta de direcciones integrada pueden solicitar al usuario la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="a82ae-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="a82ae-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="a82ae-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="a82ae-119">[salida] Puntero a un puntero a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a82ae-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a82ae-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a82ae-120">Return value</span></span>

<span data-ttu-id="a82ae-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a82ae-121">S_OK</span></span> 
  
> <span data-ttu-id="a82ae-122">La libreta de direcciones se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="a82ae-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="a82ae-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a82ae-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a82ae-124">La llamada se ha hecho correctamente, pero no se pudieron abrir los contenedores de uno o varios proveedores de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a82ae-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="a82ae-125">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="a82ae-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a82ae-126">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="a82ae-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a82ae-127">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a82ae-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a82ae-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a82ae-128">Remarks</span></span>

<span data-ttu-id="a82ae-129">El **método IMAPISession::OpenAddressBook** abre la libreta de direcciones integrada mapi, una colección de contenedores de nivel superior de todos los proveedores de libretas de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="a82ae-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="a82ae-130">El puntero que se devuelve en el  _parámetro lppAdrBook_ proporciona acceso adicional al contenido de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a82ae-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="a82ae-131">Esto permite al autor de la llamada realizar tareas como abrir contenedores individuales, buscar usuarios de mensajería y mostrar cuadros de diálogo de direcciones comunes.</span><span class="sxs-lookup"><span data-stu-id="a82ae-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a82ae-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a82ae-132">Notes to callers</span></span>

 <span data-ttu-id="a82ae-133">**OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED si no puede cargar uno o varios de los proveedores de libretas de direcciones en el perfil.</span><span class="sxs-lookup"><span data-stu-id="a82ae-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="a82ae-134">Este valor es una advertencia, no un valor de error; controlarlo como lo haría S_OK.</span><span class="sxs-lookup"><span data-stu-id="a82ae-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="a82ae-135">**OpenAddressBook** siempre devuelve un puntero válido en el parámetro  _lppAdrBook,_ independientemente del número de proveedores de libretas de direcciones que no se pudieron cargar.</span><span class="sxs-lookup"><span data-stu-id="a82ae-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="a82ae-136">Por lo tanto, siempre debe llamar al método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de la libreta de direcciones en algún momento antes de cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="a82ae-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="a82ae-137">Cuando **OpenAddressBook** devuelve MAPI_W_ERRORS_RETURNED, llame a [IMAPISession::GetLastError](imapisession-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contenga información sobre los proveedores con errores.</span><span class="sxs-lookup"><span data-stu-id="a82ae-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="a82ae-138">Se devuelve **una única estructura MAPIERROR** que contiene información proporcionada por todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="a82ae-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a82ae-139">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a82ae-139">MFCMAPI reference</span></span>

<span data-ttu-id="a82ae-140">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a82ae-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a82ae-141">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a82ae-141">**File**</span></span>|<span data-ttu-id="a82ae-142">**Función**</span><span class="sxs-lookup"><span data-stu-id="a82ae-142">**Function**</span></span>|<span data-ttu-id="a82ae-143">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a82ae-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a82ae-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="a82ae-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="a82ae-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="a82ae-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="a82ae-146">MFCMAPI usa el **método IMAPISession::OpenAddressBook** para obtener la libreta de direcciones integrada.</span><span class="sxs-lookup"><span data-stu-id="a82ae-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a82ae-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a82ae-147">See also</span></span>



[<span data-ttu-id="a82ae-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a82ae-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="a82ae-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a82ae-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="a82ae-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a82ae-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a82ae-151">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a82ae-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a82ae-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a82ae-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

