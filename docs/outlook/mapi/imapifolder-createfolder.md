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
ms.openlocfilehash: 694f7ec5715a7348c9bd90c28d14f30d43d19974
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581786"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="1e09c-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1e09c-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="1e09c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e09c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e09c-105">Crea una nueva subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1e09c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e09c-106">Parameters</span></span>

 <span data-ttu-id="1e09c-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="1e09c-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="1e09c-108">[entrada] El tipo de carpeta que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="1e09c-108">[in] The type of folder to create.</span></span> <span data-ttu-id="1e09c-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1e09c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="1e09c-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="1e09c-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="1e09c-111">Se debe crear una carpeta genérica.</span><span class="sxs-lookup"><span data-stu-id="1e09c-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="1e09c-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="1e09c-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="1e09c-113">Se debe crear una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1e09c-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="1e09c-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="1e09c-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="1e09c-115">[entrada] Un puntero a una cadena que contiene el nombre para la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="1e09c-116">Este nombre es la base para la propiedad de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="1e09c-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="1e09c-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="1e09c-118">[entrada] Un puntero a una cadena que contiene un comentario asociado a la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="1e09c-119">Esta cadena se convierte en el valor de propiedad de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="1e09c-120">Si se pasa NULL, la carpeta no tiene ningún comentario inicial.</span><span class="sxs-lookup"><span data-stu-id="1e09c-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="1e09c-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1e09c-121">_lpInterface_</span></span>
  
> <span data-ttu-id="1e09c-122">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="1e09c-123">Pasando NULL hace que el proveedor de almacenamiento de mensajes devolver la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="1e09c-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="1e09c-124">Los clientes deben pasar NULL.</span><span class="sxs-lookup"><span data-stu-id="1e09c-124">Clients must pass NULL.</span></span> <span data-ttu-id="1e09c-125">Otros autores de llamadas pueden establecer el parámetro _lpInterface_ para IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="1e09c-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="1e09c-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e09c-126">_ulFlags_</span></span>
  
> <span data-ttu-id="1e09c-127">[entrada] Una máscara de bits de indicadores que controla cómo se crea la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="1e09c-128">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1e09c-128">The following flags can be set:</span></span>
    
<span data-ttu-id="1e09c-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1e09c-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1e09c-130">Permite **CreateFolder** devolver de correctamente, posiblemente antes de que la nueva carpeta es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="1e09c-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="1e09c-131">Si la nueva carpeta no está disponible, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="1e09c-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="1e09c-132">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1e09c-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1e09c-133">El nombre de la carpeta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e09c-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="1e09c-134">Si no está establecido el indicador MAPI_UNICODE., el nombre de la carpeta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e09c-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="1e09c-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="1e09c-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="1e09c-136">Permite que el método se realice correctamente, incluso si la carpeta denominada en el parámetro _lpszFolderName_ ya existe, abra la carpeta existente que tiene ese nombre.</span><span class="sxs-lookup"><span data-stu-id="1e09c-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="1e09c-137">Tenga en cuenta que los proveedores de almacén de mensajes que permiten carpetas que tienen el mismo nombre de elemento del mismo nivel no pueden abrir una carpeta existente si existe más de uno con el nombre proporcionado.</span><span class="sxs-lookup"><span data-stu-id="1e09c-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="1e09c-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="1e09c-138">_lppFolder_</span></span>
  
> <span data-ttu-id="1e09c-139">[out] Un puntero a un puntero a la carpeta recién creada.</span><span class="sxs-lookup"><span data-stu-id="1e09c-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e09c-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e09c-140">Return value</span></span>

<span data-ttu-id="1e09c-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e09c-141">S_OK</span></span> 
  
> <span data-ttu-id="1e09c-142">La nueva carpeta se ha creado o abierto, si se establece la marca OPEN_IF_EXISTS correctamente.</span><span class="sxs-lookup"><span data-stu-id="1e09c-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="1e09c-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1e09c-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1e09c-144">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e09c-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="1e09c-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="1e09c-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="1e09c-146">Una carpeta que tiene el nombre indicado en el parámetro _lpszFolderName_ ya existe.</span><span class="sxs-lookup"><span data-stu-id="1e09c-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="1e09c-147">Los nombres de carpeta deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="1e09c-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1e09c-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e09c-148">Remarks</span></span>

<span data-ttu-id="1e09c-149">El método **IMAPIFolder::CreateFolder** crea una subcarpeta en la carpeta actual y asigna un identificador de entrada a la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="1e09c-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1e09c-150">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1e09c-150">Notes to callers</span></span>

<span data-ttu-id="1e09c-151">Cuando se devuelve **CreateFolder** , tenga en cuenta que es posible que el identificador de entrada para la nueva carpeta no estén disponible.</span><span class="sxs-lookup"><span data-stu-id="1e09c-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="1e09c-152">Algunos proveedores de almacén de mensajes no hace los identificadores de entrada disponible hasta después de llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la carpeta nueva para guardar de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="1e09c-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="1e09c-153">Esto es especialmente útil si ha establecido el indicador MAPI_DEFERRED_ERRORS.</span><span class="sxs-lookup"><span data-stu-id="1e09c-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="1e09c-154">Tenga en cuenta que algunos proveedores de almacenes de mensaje elija siempre el parámetro _lppFolder_ interfaz estándar de la carpeta, independientemente del valor que se pasa para el parámetro _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="1e09c-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="1e09c-155">Debido a que el puntero de interfaz que se devuelve no puede ser del tipo que se esperaba, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta nueva para recuperar la propiedad **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1e09c-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="1e09c-156">Si es necesario, convertir el puntero a un tipo más apropiado antes de realizar otras llamadas.</span><span class="sxs-lookup"><span data-stu-id="1e09c-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="1e09c-157">La mayoría de los proveedores de almacén de mensajes requieren el nombre de la nueva carpeta por qué ser únicos con respecto a los nombres de las carpetas del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="1e09c-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="1e09c-158">Ser capaz de controlar el valor de error MAPI_E_COLLISION, que se devuelve si no se sigue esta regla.</span><span class="sxs-lookup"><span data-stu-id="1e09c-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="1e09c-159">Para determinar el identificador de entrada de la carpeta recién creada, llamar al método **IMAPIProp::GetProps** de la carpeta nueva para recuperar su propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1e09c-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1e09c-160">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1e09c-160">MFCMAPI reference</span></span>

<span data-ttu-id="1e09c-161">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1e09c-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1e09c-162">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1e09c-162">**File**</span></span>|<span data-ttu-id="1e09c-163">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="1e09c-163">**Function**</span></span>|<span data-ttu-id="1e09c-164">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1e09c-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e09c-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1e09c-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="1e09c-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="1e09c-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="1e09c-167">MFCMAPI utiliza el método **CMsgStoreDlg::OnCreateSubFolder** para crear nuevas carpetas en MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="1e09c-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e09c-168">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1e09c-168">See also</span></span>



[<span data-ttu-id="1e09c-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="1e09c-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="1e09c-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1e09c-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="1e09c-171">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1e09c-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

