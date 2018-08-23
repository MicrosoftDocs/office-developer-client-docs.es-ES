---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 26550691ef959fa7cefa83827dd1391538bd2d38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588177"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="9b395-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="9b395-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="9b395-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b395-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b395-105">Proporciona acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9b395-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="9b395-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b395-106">Parameters</span></span>

 <span data-ttu-id="9b395-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9b395-107">_lpInterface_</span></span>
  
> <span data-ttu-id="9b395-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9b395-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="9b395-109">Los valores válidos son NULL, que indica la interfaz de la libreta de direcciones estándar [IAddrBook](iaddrbookimapiprop.md)y IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="9b395-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="9b395-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b395-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9b395-111">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9b395-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9b395-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="9b395-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="9b395-113">[out] Un puntero a un puntero a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9b395-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b395-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b395-114">Return value</span></span>

<span data-ttu-id="9b395-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b395-115">S_OK</span></span> 
  
> <span data-ttu-id="9b395-116">Le ha proporcionado el acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9b395-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="9b395-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="9b395-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="9b395-118">La llamada se ha realizado correctamente, pero no se podrían cargados uno o más proveedores de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9b395-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="9b395-119">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="9b395-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9b395-120">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="9b395-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9b395-121">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9b395-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b395-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b395-122">Remarks</span></span>

<span data-ttu-id="9b395-123">El método **IMAPISupport::OpenAddressBook** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="9b395-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="9b395-124">Proveedores de servicios, normalmente acoplado mensaje almacén y los proveedores de transporte, llame a **OpenAddressBook** para obtener acceso a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9b395-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="9b395-125">El puntero **IAddrBook** devuelto se puede usar para una gran variedad de tareas de la libreta de direcciones, incluida la apertura de contenedores de libretas de direcciones, búsqueda de usuarios de mensajería y presentación de los cuadros de diálogo de dirección.</span><span class="sxs-lookup"><span data-stu-id="9b395-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b395-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9b395-126">Notes to callers</span></span>

 <span data-ttu-id="9b395-127">**OpenAddressBook** puede devolver MAPI_W_ERRORS_RETURNED si no puede cargar uno o varios de los proveedores de la libreta de direcciones en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="9b395-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="9b395-128">Este valor es una advertencia y se debe tratar la llamada como correcta.</span><span class="sxs-lookup"><span data-stu-id="9b395-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="9b395-129">Incluso si todos los proveedores de la libreta de direcciones no se pudo cargar, **OpenAddressBook** aún se realiza correctamente, devolver MAPI_W_ERRORS_RETURNED y un puntero **IAddrBook** en el parámetro _lppAdrBook_ .</span><span class="sxs-lookup"><span data-stu-id="9b395-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="9b395-130">Debido a que **OpenAddressBook** siempre devuelve un puntero **IAddrBook** válido, debe liberar cuando haya terminado de usarlo.</span><span class="sxs-lookup"><span data-stu-id="9b395-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="9b395-131">Si no se pudo cargar uno o más proveedores de libreta de direcciones, llame a [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obtener una estructura [MAPIERROR](mapierror.md) que contiene información sobre los proveedores que no se ha cargado.</span><span class="sxs-lookup"><span data-stu-id="9b395-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b395-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9b395-132">See also</span></span>



[<span data-ttu-id="9b395-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9b395-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="9b395-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="9b395-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="9b395-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b395-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

