---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436765"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="a974a-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="a974a-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="a974a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a974a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a974a-105">Crea una subcarpeta nueva.</span><span class="sxs-lookup"><span data-stu-id="a974a-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="a974a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a974a-106">Parameters</span></span>

 <span data-ttu-id="a974a-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="a974a-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="a974a-108">a El tipo de carpeta que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="a974a-108">[in] The type of folder to create.</span></span> <span data-ttu-id="a974a-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="a974a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="a974a-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="a974a-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="a974a-111">Se debe crear una carpeta genérica.</span><span class="sxs-lookup"><span data-stu-id="a974a-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="a974a-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="a974a-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="a974a-113">Debe crearse una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a974a-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="a974a-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="a974a-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="a974a-115">a Un puntero a una cadena que contiene el nombre de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="a974a-116">Este nombre es la base de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="a974a-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="a974a-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="a974a-118">a Un puntero a una cadena que contiene un comentario asociado a la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="a974a-119">Esta cadena se convierte en el valor de la propiedad **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="a974a-120">Si se pasa NULL, la carpeta no tiene comentario inicial.</span><span class="sxs-lookup"><span data-stu-id="a974a-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="a974a-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a974a-121">_lpInterface_</span></span>
  
> <span data-ttu-id="a974a-122">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="a974a-123">Al pasar NULL, el proveedor de almacén de mensajes devuelve la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="a974a-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="a974a-124">Los clientes deben pasar NULL.</span><span class="sxs-lookup"><span data-stu-id="a974a-124">Clients must pass NULL.</span></span> <span data-ttu-id="a974a-125">Otros llamadores pueden establecer el parámetro _lpInterface_ en IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="a974a-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="a974a-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a974a-126">_ulFlags_</span></span>
  
> <span data-ttu-id="a974a-127">a Una máscara de máscara de marcas que controla cómo se crea la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="a974a-128">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="a974a-128">The following flags can be set:</span></span>
    
<span data-ttu-id="a974a-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a974a-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a974a-130">Permite que **CreateFolder** vuelva correctamente, posiblemente antes de que la nueva carpeta esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="a974a-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="a974a-131">Si la nueva carpeta no está disponible, realizar una llamada subsiguiente a ella puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="a974a-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="a974a-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a974a-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a974a-133">El nombre de la carpeta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a974a-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="a974a-134">Si no se establece la marca MAPI_UNICODE, el nombre de la carpeta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a974a-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="a974a-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="a974a-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="a974a-136">Permite que el método tenga éxito incluso si la carpeta especificada en el parámetro _lpszFolderName_ ya existe abriendo la carpeta existente que tiene ese nombre.</span><span class="sxs-lookup"><span data-stu-id="a974a-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="a974a-137">Tenga en cuenta que es posible que los proveedores de almacenamiento de mensajes que permiten que las carpetas relacionadas tengan el mismo nombre no puedan abrir una carpeta existente si existe más de una con el nombre proporcionado.</span><span class="sxs-lookup"><span data-stu-id="a974a-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="a974a-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="a974a-138">_lppFolder_</span></span>
  
> <span data-ttu-id="a974a-139">contempla Un puntero a un puntero a la carpeta que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="a974a-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a974a-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a974a-140">Return value</span></span>

<span data-ttu-id="a974a-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="a974a-141">S_OK</span></span> 
  
> <span data-ttu-id="a974a-142">La nueva carpeta se ha creado o abierto correctamente, si se ha establecido la marca OPEN_IF_EXISTS.</span><span class="sxs-lookup"><span data-stu-id="a974a-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="a974a-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a974a-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a974a-144">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="a974a-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="a974a-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="a974a-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="a974a-146">Ya existe una carpeta con el nombre especificado en el parámetro _lpszFolderName_ .</span><span class="sxs-lookup"><span data-stu-id="a974a-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="a974a-147">Los nombres de carpeta deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="a974a-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a974a-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a974a-148">Remarks</span></span>

<span data-ttu-id="a974a-149">El método **IMAPIFolder:: CreateFolder** crea una subcarpeta en la carpeta actual y asigna un identificador de entrada a la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="a974a-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a974a-150">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a974a-150">Notes to callers</span></span>

<span data-ttu-id="a974a-151">Cuando **CreateFolder** Return, tenga en cuenta que es posible que el identificador de entrada para la nueva carpeta no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="a974a-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="a974a-152">Algunos proveedores de almacenamiento de mensajes no hacen que los identificadores de entrada estén disponibles hasta que se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la nueva carpeta para guardarlo de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="a974a-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="a974a-153">Esto es especialmente cierto si ha establecido la marca MAPI_DEFERRED_ERRORS.</span><span class="sxs-lookup"><span data-stu-id="a974a-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="a974a-154">Tenga en cuenta que algunos proveedores de almacenamiento de mensajes siempre señalan el parámetro _lppFolder_ a la interfaz estándar de la carpeta, independientemente del valor que se pase para el parámetro _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="a974a-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="a974a-155">Dado que el puntero de interfaz que se devuelve puede que no sea del tipo que espera, llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la nueva carpeta para recuperar la propiedad **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a974a-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="a974a-156">Si es necesario, convierta el puntero en un tipo más apropiado antes de realizar otras llamadas.</span><span class="sxs-lookup"><span data-stu-id="a974a-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="a974a-157">La mayoría de los proveedores de almacenamiento de mensajes requieren que el nombre de la nueva carpeta sea único con respecto a los nombres de sus carpetas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a974a-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="a974a-158">Ser capaz de controlar el valor de error MAPI_E_COLLISION, que se devuelve si no se sigue esta regla.</span><span class="sxs-lookup"><span data-stu-id="a974a-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="a974a-159">Para determinar el identificador de entrada de la carpeta recién creada, llame al método **IMAPIProp:: GetProps** de la nueva carpeta para recuperar \*\*\*\* su propiedad ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a974a-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a974a-160">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a974a-160">MFCMAPI reference</span></span>

<span data-ttu-id="a974a-161">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a974a-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a974a-162">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a974a-162">**File**</span></span>|<span data-ttu-id="a974a-163">**Función**</span><span class="sxs-lookup"><span data-stu-id="a974a-163">**Function**</span></span>|<span data-ttu-id="a974a-164">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a974a-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a974a-165">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a974a-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="a974a-166">CMsgStoreDlg:: OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="a974a-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="a974a-167">MFCMAPI usa el método **CMsgStoreDlg:: OnCreateSubFolder** para crear nuevas carpetas en MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="a974a-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a974a-168">Ver también</span><span class="sxs-lookup"><span data-stu-id="a974a-168">See also</span></span>



[<span data-ttu-id="a974a-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a974a-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="a974a-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a974a-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="a974a-171">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a974a-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

