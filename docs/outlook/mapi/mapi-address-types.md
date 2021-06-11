---
title: Tipos de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405439"
---
# <a name="mapi-address-types"></a><span data-ttu-id="88786-103">Tipos de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="88786-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="88786-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88786-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88786-105">Cada usuario de mensajería está asociado con un tipo de dirección, una cadena de caracteres que describe el formato de la dirección del usuario que se almacena en la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="88786-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="88786-106">Los tipos de direcciones se asignan a formatos de dirección.</span><span class="sxs-lookup"><span data-stu-id="88786-106">Address types map to address formats.</span></span> <span data-ttu-id="88786-107">Es decir, al ver el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección adecuada para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="88786-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="88786-108">Por ejemplo, el  `SMTP` tipo de dirección especifica la dirección de Internet estándar:</span><span class="sxs-lookup"><span data-stu-id="88786-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="88786-109">Además, el `EX` tipo de dirección especifica una Exchange Server dirección.</span><span class="sxs-lookup"><span data-stu-id="88786-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="88786-110">Todas las entradas de la libreta de direcciones deben tener un tipo de dirección válido.</span><span class="sxs-lookup"><span data-stu-id="88786-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="88786-111">Los clientes requieren que sus usuarios especifiquen un tipo de dirección al crear un tipo de destinatario personalizado no admitido por el proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="88786-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="88786-112">Para las entradas que admiten, los proveedores de libreta de direcciones deben proporcionar tipos de direcciones válidos.</span><span class="sxs-lookup"><span data-stu-id="88786-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="88786-113">MAPI define solo un tipo de dirección: MAPIPDL, que significa lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="88786-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="88786-114">Para obtener una lista de los tipos de direcciones admitidos por todos los proveedores de transporte de la sesión, las aplicaciones cliente llaman al método **IMAPISession::EnumAdrTypes.**</span><span class="sxs-lookup"><span data-stu-id="88786-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="88786-115">Para obtener más información, [vea IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="88786-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

