---
title: Propiedad Ocultar opción de actualización de reunión
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816961"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="b24d8-103">Propiedad Ocultar opción de actualización de reunión</span><span class="sxs-lookup"><span data-stu-id="b24d8-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="b24d8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b24d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b24d8-105">Oculta la opción para enviar actualizaciones de reunión a los asistentes sólo se ha agregado o eliminados.</span><span class="sxs-lookup"><span data-stu-id="b24d8-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b24d8-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b24d8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b24d8-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="b24d8-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="b24d8-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="b24d8-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="b24d8-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="b24d8-109">Created by:</span></span>  <br/> |<span data-ttu-id="b24d8-110">Proveedor de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="b24d8-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="b24d8-111">Tener acceso a ella:</span><span class="sxs-lookup"><span data-stu-id="b24d8-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="b24d8-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="b24d8-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="b24d8-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="b24d8-113">Property type:</span></span>  <br/> |<span data-ttu-id="b24d8-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b24d8-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b24d8-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="b24d8-115">Access type:</span></span>  <br/> |<span data-ttu-id="b24d8-116">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b24d8-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b24d8-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b24d8-117">Remarks</span></span>

<span data-ttu-id="b24d8-118">Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="b24d8-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="b24d8-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta.</span><span class="sxs-lookup"><span data-stu-id="b24d8-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="b24d8-120">Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b24d8-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="b24d8-121">Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="b24d8-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b24d8-122">Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="b24d8-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b24d8-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="b24d8-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="b24d8-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b24d8-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="b24d8-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="b24d8-125">ulKind:</span></span>  <br/> |<span data-ttu-id="b24d8-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b24d8-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="b24d8-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="b24d8-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="b24d8-128">L "urn: schemas-microsoft-com:office:outlook #allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="b24d8-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="b24d8-129">Un proveedor de almacenamiento que usa un servidor para enviar actualizaciones de reunión puede modificar el cuadro de diálogo **Enviar actualización a los asistentes** .</span><span class="sxs-lookup"><span data-stu-id="b24d8-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="b24d8-130">Esta funcionalidad es útil porque cuando el servidor envía una actualización de la reunión, el servidor no sabe qué asistentes se han agregado o eliminado por el usuario con respecto a la convocatoria de reunión inicial.</span><span class="sxs-lookup"><span data-stu-id="b24d8-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="b24d8-131">Cuando esta propiedad es **true**, la opción **Enviar actualización únicamente para los asistentes se ha agregado o eliminados** no se muestra en el cuadro de diálogo **Enviar actualización a los asistentes** .</span><span class="sxs-lookup"><span data-stu-id="b24d8-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="b24d8-132">Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1, o si su valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="b24d8-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

