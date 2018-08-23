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
ms.openlocfilehash: c8bd8c7fb2ff5a030cd96e4c3ac2bbb4b6b16ce5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571461"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="7174a-103">Propiedad canónica PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="7174a-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="7174a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7174a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7174a-105">Contiene una tabla de un mensaje almacén de configuración de la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="7174a-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7174a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7174a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7174a-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="7174a-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="7174a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7174a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7174a-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="7174a-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="7174a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7174a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7174a-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="7174a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7174a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7174a-112">Area:</span></span>  <br/> |<span data-ttu-id="7174a-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="7174a-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7174a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7174a-114">Remarks</span></span>

<span data-ttu-id="7174a-115">Esta propiedad puede ser en las operaciones de [IMAPIProp::CopyTo](imapiprop-copyto.md) incluyen o excluyen de operaciones de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="7174a-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="7174a-116">Como una propiedad de tipo pt Object, no se correctamente puede recuperar mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) ; el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , que solicita la interfaz con el identificador de IID_IMAPITable debe tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="7174a-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="7174a-117">Proveedores de servicios deben identificarlo al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) si está establecida, pero puede, opcionalmente, identificarlo o no, si no está establecido.</span><span class="sxs-lookup"><span data-stu-id="7174a-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="7174a-118">Para recuperar el contenido de la tabla, una aplicación de cliente debe llamar al método de [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="7174a-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="7174a-119">Para obtener más información, vea [Recibir carpeta tablas](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7174a-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="7174a-120">Esta propiedad contiene una tabla de asignaciones de las carpetas de recepción para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7174a-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="7174a-121">Al llamar a **OpenProperty** en esta propiedad es equivalente a llamar a **GetReceiveFolderTable** en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7174a-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7174a-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7174a-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7174a-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7174a-123">Header files</span></span>

<span data-ttu-id="7174a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7174a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7174a-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7174a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7174a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7174a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7174a-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7174a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7174a-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7174a-128">See also</span></span>



[<span data-ttu-id="7174a-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7174a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7174a-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7174a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7174a-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7174a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7174a-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7174a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

