---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817133"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="ba589-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ba589-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="ba589-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba589-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba589-105">Establece el contenedor especificado como el contenedor de la libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ba589-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ba589-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba589-106">Parameters</span></span>

 <span data-ttu-id="ba589-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ba589-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ba589-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ba589-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ba589-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ba589-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ba589-110">[entrada] Un puntero al identificador de entrada del contenedor de la libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ba589-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba589-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba589-111">Return value</span></span>

<span data-ttu-id="ba589-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba589-112">S_OK</span></span> 
  
> <span data-ttu-id="ba589-113">Se estableció correctamente en el contenedor de la libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ba589-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba589-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba589-114">Remarks</span></span>

<span data-ttu-id="ba589-115">Los clientes y proveedores de servicios de llamar al método **SetDefaultDir** para establecer un nuevo contenedor de libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ba589-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="ba589-116">El contenedor predeterminado es el contenedor que ve el usuario que se muestra en la libreta de direcciones cuando se abre por primera vez la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ba589-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="ba589-117">**SetDefaultDir** guarda el contenedor predeterminado como una entrada en el perfil.</span><span class="sxs-lookup"><span data-stu-id="ba589-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="ba589-118">El contenedor permanece como el valor predeterminado hasta que se realiza otra llamada a **SetDefaultDir** en la misma sesión o en otra sesión, o se ha quitado el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ba589-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ba589-119">La propiedad [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) corresponde a la opción **elija automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ba589-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="ba589-120">Cuando esta propiedad existe en la sección de perfil [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) y se establece en **true**, el cuadro de diálogo de la libreta de direcciones ya no se establece de forma predeterminada en el contenedor especificado por **SetDefaultDir**, pero elige una libreta de direcciones que considera de Microsoft Outlook adecuada para el contexto en el que se muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ba589-120">When this property exists in the [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="ba589-121">Tenga en cuenta que esto puede producir una mala experiencia para los proveedores de libreta de direcciones de otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="ba589-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba589-122">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ba589-122">MFCMAPI reference</span></span>

<span data-ttu-id="ba589-123">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ba589-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba589-124">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ba589-124">**File**</span></span>|<span data-ttu-id="ba589-125">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ba589-125">**Function**</span></span>|<span data-ttu-id="ba589-126">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ba589-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba589-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ba589-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="ba589-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ba589-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="ba589-129">MFCMAPI usa el método **SetDefaultDir** para realizar el contenedor de la libreta de direcciones especificado en el valor predeterminado uno.</span><span class="sxs-lookup"><span data-stu-id="ba589-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba589-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba589-130">See also</span></span>



[<span data-ttu-id="ba589-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="ba589-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="ba589-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="ba589-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="ba589-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="ba589-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="ba589-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ba589-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="ba589-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ba589-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ba589-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ba589-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

