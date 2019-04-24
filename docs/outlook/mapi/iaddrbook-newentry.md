---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336718"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="370d5-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="370d5-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="370d5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="370d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="370d5-105">Agrega un nuevo destinatario a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="370d5-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="370d5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="370d5-106">Parameters</span></span>

 <span data-ttu-id="370d5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="370d5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="370d5-108">a Identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="370d5-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="370d5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="370d5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="370d5-110">a Máscara de máscara de marcadores que controla el tipo de texto que se usa.</span><span class="sxs-lookup"><span data-stu-id="370d5-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="370d5-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="370d5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="370d5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="370d5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="370d5-113">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="370d5-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="370d5-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="370d5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="370d5-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="370d5-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="370d5-116">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="370d5-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="370d5-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="370d5-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="370d5-118">a Un puntero al identificador de entrada del contenedor donde se agregará el nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="370d5-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="370d5-119">Si el parámetro _cbEIDContainer_ es cero, el método **NEWENTRY** devuelve un identificador de entrada de destinatario y una lista de plantillas como si se hubiera llamado al método [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) .</span><span class="sxs-lookup"><span data-stu-id="370d5-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="370d5-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="370d5-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="370d5-121">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEIDNewEntryTpl_ .</span><span class="sxs-lookup"><span data-stu-id="370d5-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="370d5-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="370d5-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="370d5-123">a Un puntero a una plantilla de uso único que se usará para crear el nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="370d5-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="370d5-124">Si _cbEIDNewEntryTpl_ es cero y _lpEIDNewEntryTpl_ es null, **NEWENTRY** muestra un cuadro de diálogo con el que el usuario puede seleccionar de una lista de plantillas para agregar nuevas entradas.</span><span class="sxs-lookup"><span data-stu-id="370d5-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="370d5-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="370d5-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="370d5-126">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="370d5-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="370d5-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="370d5-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="370d5-128">contempla Un puntero a un puntero al identificador de entrada del nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="370d5-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="370d5-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="370d5-129">Return value</span></span>

<span data-ttu-id="370d5-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="370d5-130">S_OK</span></span> 
  
> <span data-ttu-id="370d5-131">La nueva entrada de la libreta de direcciones se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="370d5-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="370d5-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="370d5-132">Remarks</span></span>

<span data-ttu-id="370d5-133">El método **NEWENTRY** crea una nueva entrada de la libreta de direcciones, que se agrega directamente en un contenedor o que se va a usar para dirigir un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="370d5-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="370d5-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="370d5-134">Notes to callers</span></span>

<span data-ttu-id="370d5-135">Si desea que la nueva entrada se agregue a un contenedor específico, establezca _lpEIDContainer_ en el identificador de entrada del contenedor y _cbEIDContainer_ en el recuento de bytes en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="370d5-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="370d5-136">Si desea que la nueva entrada se agregue a la lista de destinatarios de un mensaje saliente, establezca _lpEIDContainer_ en NULL y _cbEIDContainer_ en cero.</span><span class="sxs-lookup"><span data-stu-id="370d5-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="370d5-137">Si desea permitir que el usuario de una aplicación cliente seleccione el tipo de entrada que se va a crear, pase cero en _cbEIDNewEntryTpl_ y null en _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="370d5-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="370d5-138">El método **NEWENTRY** muestra la tabla de una sola desactivación, una lista de plantillas admitidas por MAPI y por cada proveedor de la libreta de direcciones en la sesión.</span><span class="sxs-lookup"><span data-stu-id="370d5-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="370d5-139">Cada plantilla puede crear una entrada de destinatario para uno o más tipos de dirección.</span><span class="sxs-lookup"><span data-stu-id="370d5-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="370d5-140">Si desea conservar el identificador de entrada de la nueva entrada, pase punteros válidos en los parámetros _lpcbEIDNewEntry_ y _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="370d5-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="370d5-141">Usted es responsable de liberar este identificador de entrada cuando termine con él llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="370d5-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="370d5-142">Para usar una plantilla determinada para agregar una nueva entrada a un contenedor modificable, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="370d5-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="370d5-143">Llame al método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir el contenedor de destino y establezca el parámetro _lpEntryID_ en el identificador de entrada del contenedor.</span><span class="sxs-lookup"><span data-stu-id="370d5-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="370d5-144">Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor de destino y establezca el parámetro _ulPropTag_ en **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) y el parámetro _lpiid_ en IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="370d5-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="370d5-145">El contenedor devolverá una tabla única en la que se enumeran todas las plantillas que admite para crear nuevas entradas.</span><span class="sxs-lookup"><span data-stu-id="370d5-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="370d5-146">Recupere la fila que representa la plantilla para el tipo concreto de entrada que desea crear.</span><span class="sxs-lookup"><span data-stu-id="370d5-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="370d5-147">La columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica el tipo de dirección que es compatible con la plantilla.</span><span class="sxs-lookup"><span data-stu-id="370d5-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="370d5-148">Llame al método **NEWENTRY** y establezca _lpEIDNewEntryTpl_ en el identificador de entrada de la plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="370d5-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="370d5-149">El identificador de entrada será la columna \*\*\*\* 1 ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila de la plantilla en la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="370d5-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="370d5-150">Pase cero en _cbEIDContainer_ y null en _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="370d5-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="370d5-151">Pase un puntero válido en el parámetro _lppEIDNewEntry_ si desea conservar el identificador de entrada de la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="370d5-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="370d5-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="370d5-152">See also</span></span>



[<span data-ttu-id="370d5-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="370d5-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="370d5-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="370d5-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="370d5-155">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="370d5-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="370d5-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="370d5-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

