---
title: Propiedad canónica PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415057"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="89aae-103">Propiedad canónica PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="89aae-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="89aae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89aae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89aae-105">Contiene una tabla de la configuración de la carpeta de recepción de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="89aae-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89aae-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="89aae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89aae-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="89aae-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="89aae-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="89aae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89aae-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="89aae-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="89aae-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="89aae-110">Data type:</span></span>  <br/> |<span data-ttu-id="89aae-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="89aae-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="89aae-112">Área:</span><span class="sxs-lookup"><span data-stu-id="89aae-112">Area:</span></span>  <br/> |<span data-ttu-id="89aae-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="89aae-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89aae-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89aae-114">Remarks</span></span>

<span data-ttu-id="89aae-115">Esta propiedad puede excluirse en operaciones [IMAPIProp::CopyTo](imapiprop-copyto.md) o incluirse en [operaciones IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="89aae-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="89aae-116">Como propiedad de tipo PT_OBJECT, el método [IMAPIProp::GetProps](imapiprop-getprops.md) no puede recuperarla correctamente; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) debe tener acceso a su contenido, solicitando la interfaz con identificador IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="89aae-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="89aae-117">Los proveedores de servicios deben notificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecido, pero opcionalmente pueden notificarlo o no si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="89aae-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="89aae-118">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="89aae-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="89aae-119">Para obtener más información, vea [Tablas de carpetas de recepción.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="89aae-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="89aae-120">Esta propiedad contiene una tabla de asignaciones de las carpetas de recepción para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="89aae-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="89aae-121">Llamar **a OpenProperty** en esta propiedad equivale a llamar a **GetReceiveFolderTable** en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="89aae-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="89aae-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89aae-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89aae-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="89aae-123">Header files</span></span>

<span data-ttu-id="89aae-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89aae-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="89aae-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="89aae-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="89aae-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89aae-126">Mapitags.h</span></span>
  
> <span data-ttu-id="89aae-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="89aae-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89aae-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89aae-128">See also</span></span>



[<span data-ttu-id="89aae-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89aae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89aae-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="89aae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89aae-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="89aae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89aae-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="89aae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

