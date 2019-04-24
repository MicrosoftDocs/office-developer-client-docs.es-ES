---
title: Establecer el orden de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339392"
---
# <a name="setting-transport-order"></a><span data-ttu-id="859c1-103">Establecer el orden de transporte</span><span class="sxs-lookup"><span data-stu-id="859c1-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="859c1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="859c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="859c1-105">La cola MAPI asigna la responsabilidad de los mensajes salientes en función de los tipos de direcciones y los identificadores que los proveedores de transporte declaran que pueden controlar.</span><span class="sxs-lookup"><span data-stu-id="859c1-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="859c1-106">Los proveedores de transporte publican una lista de los identificadores y los tipos de direcciones compatibles, almacenados en las estructuras **MAPIUID** , cuando MAPI llama a su método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , directamente después del inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="859c1-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="859c1-107">El tipo de dirección de un destinatario se almacena en su propiedad **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="859c1-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="859c1-108">El registro para un tipo de dirección indica a MAPI que el proveedor de transporte puede entregar a los destinatarios con su propiedad **PR_ADDRTYPE** establecida en el tipo de dirección registrado.</span><span class="sxs-lookup"><span data-stu-id="859c1-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="859c1-109">De forma similar, el registro para un **MAPIUID** indica que el proveedor de transporte puede entregar a los destinatarios representados mediante identificadores de entrada con el **MAPIUID**registrado.</span><span class="sxs-lookup"><span data-stu-id="859c1-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="859c1-110">La mayoría de los proveedores de transporte se registran para uno o más tipos de dirección; pocos registros de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="859c1-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="859c1-111">Los proveedores de transporte que están estrechamente acoplados con un proveedor de libreta de direcciones y entienden su formato de identificador de entrada se pueden registrar para controlar los mensajes mediante **MAPIUID**, con lo que se mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="859c1-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="859c1-112">Estos proveedores de transporte estrechamente acoplados pueden extraer la dirección de correo electrónico del destinatario y otra información necesaria del identificador de entrada sin tener que abrirlo con una llamada **IMAPISupport:: OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="859c1-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="859c1-113">MAPI mantiene un pedido para los proveedores de transporte, que se usa cuando se han registrado varios proveedores de transporte para el mismo tipo de dirección o **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="859c1-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="859c1-114">Puede invalidar este orden llamando a [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) y pasando una lista ordenada de los **MAPIUID**de todos los proveedores de transporte activos señalados por el parámetro _lpUIDList_ .:</span><span class="sxs-lookup"><span data-stu-id="859c1-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="859c1-115">Para recuperar una lista de todos los tipos de direcciones que puede controlar uno de los proveedores de transporte activos, llame a [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="859c1-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="859c1-116">**EnumAdrTypes** devuelve una matriz de cadenas que describe los tipos de direcciones admitidos por los proveedores de transporte que están activos en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="859c1-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

