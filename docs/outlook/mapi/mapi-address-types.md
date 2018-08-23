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
ms.openlocfilehash: 80e933f5723746dbaeb39271cc813eb0ea56a705
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571188"
---
# <a name="mapi-address-types"></a><span data-ttu-id="e3e10-103">Tipos de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="e3e10-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="e3e10-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3e10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3e10-105">Todos los usuarios de mensajería está asociado con un tipo de dirección, una cadena de caracteres que describe el formato de la dirección del usuario que se almacena en la propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e3e10-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="e3e10-106">Tipos de direcciones que se asignan a formatos de dirección.</span><span class="sxs-lookup"><span data-stu-id="e3e10-106">Address types map to address formats.</span></span> <span data-ttu-id="e3e10-107">Es decir, mirando en el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección apropiada para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="e3e10-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="e3e10-108">Por ejemplo, el `SMTP` tipo de dirección especifica la dirección de Internet estándar:</span><span class="sxs-lookup"><span data-stu-id="e3e10-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="e3e10-109">Y, el `EX` tipo de dirección especifica una dirección de servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3e10-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="e3e10-110">Todas las entradas de la libreta de direcciones deben tener un tipo de dirección válida.</span><span class="sxs-lookup"><span data-stu-id="e3e10-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="e3e10-111">Los clientes requieren que sus usuarios especificar un tipo de dirección al crear un tipo de destinatario personalizado no compatible con el proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e3e10-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="e3e10-112">Para las entradas que admiten, se requieren los proveedores de la libreta de direcciones para proporcionar tipos de direcciones válidas.</span><span class="sxs-lookup"><span data-stu-id="e3e10-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="e3e10-113">MAPI define el tipo de una sola dirección: MAPIPDL, que significa de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="e3e10-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="e3e10-114">Para obtener una lista de los tipos de direcciones compatibles con todos los proveedores de transporte en la sesión, las aplicaciones cliente de llaman al método **IMAPISession:: EnumAdrTypes** .</span><span class="sxs-lookup"><span data-stu-id="e3e10-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="e3e10-115">Para obtener más información, vea [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="e3e10-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

