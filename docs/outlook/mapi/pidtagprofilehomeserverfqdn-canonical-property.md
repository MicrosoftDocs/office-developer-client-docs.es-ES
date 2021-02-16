---
title: Propiedad canónica PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341597"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="c81c5-103">Propiedad canónica PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="c81c5-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="c81c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c81c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c81c5-105">Habilita la autenticación Kerberos de una configuración de perfil.</span><span class="sxs-lookup"><span data-stu-id="c81c5-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="c81c5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c81c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c81c5-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="c81c5-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="c81c5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c81c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c81c5-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="c81c5-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="c81c5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c81c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="c81c5-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c81c5-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c81c5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c81c5-112">Area:</span></span>  <br/> |<span data-ttu-id="c81c5-113">Configuración de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="c81c5-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c81c5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c81c5-114">Remarks</span></span>

<span data-ttu-id="c81c5-115">Establecer esta propiedad en el nombre de dominio del servidor de directorio del usuario permite la conexión directa con el controlador de dominio (DC), que es necesario para un perfil que se ha configurado para usar la autenticación Kerberos en Microsoft Exchange Server 2007 y versiones anteriores, estableciendo **RPC_C_AUTHN_GSS_KERBEROS** en **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="c81c5-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c81c5-116">Microsoft Exchange Server 2010 y Exchange Server 2013 controlan las llamadas de libreta de direcciones realizadas al servidor de acceso de cliente de forma diferente a la forma en que Exchange Server 2007 y versiones anteriores las controlan.</span><span class="sxs-lookup"><span data-stu-id="c81c5-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="c81c5-117">El proceso DSProxy ya no se usa, por lo que la autenticación Kerberos puede ser correcta.</span><span class="sxs-lookup"><span data-stu-id="c81c5-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="c81c5-118">Sin embargo, el cliente seguiría comunicándose con el servidor exchange en lugar de directamente con el DC, lo que puede que no desee: la configuración PR_PROFILE_HOME_SERVER_FQDN **evita** esto.</span><span class="sxs-lookup"><span data-stu-id="c81c5-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c81c5-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c81c5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c81c5-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c81c5-120">Protocol specifications</span></span>

<span data-ttu-id="c81c5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c81c5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c81c5-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c81c5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c81c5-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c81c5-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c81c5-124">Especifica las operaciones permitidas para los objetos principales del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c81c5-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c81c5-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c81c5-125">Header files</span></span>

<span data-ttu-id="c81c5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c81c5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c81c5-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c81c5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c81c5-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c81c5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c81c5-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c81c5-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c81c5-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c81c5-130">See also</span></span>



[<span data-ttu-id="c81c5-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c81c5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c81c5-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="c81c5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c81c5-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c81c5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c81c5-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c81c5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

