---
title: Configuración del orden de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433601"
---
# <a name="setting-transport-order"></a><span data-ttu-id="71af8-103">Configuración del orden de transporte</span><span class="sxs-lookup"><span data-stu-id="71af8-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="71af8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71af8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71af8-105">La cola MAPI asigna la responsabilidad de los mensajes salientes en función de los tipos de direcciones e identificadores que los proveedores de transporte declaran que pueden controlar.</span><span class="sxs-lookup"><span data-stu-id="71af8-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="71af8-106">Los proveedores de transporte publican una lista de identificadores y tipos de direcciones admitidos (almacenados en estructuras **MAPIUID)** cuando MAPI llama a su método [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) directamente después del inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="71af8-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="71af8-107">El tipo de dirección de un destinatario se almacena **en su propiedad PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="71af8-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="71af8-108">El registro de un tipo de dirección indica a MAPI que el proveedor de transporte puede entregar a los destinatarios con su propiedad **PR_ADDRTYPE** establecida en el tipo de dirección registrada.</span><span class="sxs-lookup"><span data-stu-id="71af8-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="71af8-109">Del mismo modo, el registro de **mapiuid** indica que el proveedor de transporte puede entregar a los destinatarios representados por identificadores de entrada con **el MAPIUID registrado**.</span><span class="sxs-lookup"><span data-stu-id="71af8-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="71af8-110">La mayoría de los proveedores de transporte se registran para uno o más tipos de direcciones; pocos se registran **por MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="71af8-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="71af8-111">Los proveedores de transporte estrechamente unidos a un proveedor de libreta de direcciones y que comprenden su formato de identificador de entrada pueden registrarse para controlar los mensajes mediante **MAPIUID,** lo que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="71af8-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="71af8-112">Estos proveedores de transporte estrechamente acoplados pueden extraer la dirección de correo electrónico del destinatario y otra información necesaria del identificador de entrada sin tener que abrirlo con una llamada **IMAPISupport::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="71af8-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="71af8-113">MAPI mantiene un orden para los proveedores de transporte, que se usa cuando varios proveedores de transporte se han registrado para el mismo tipo de dirección o **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="71af8-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="71af8-114">Puede invalidar este orden llamando a [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) y pasando una lista ordenada de **los MAPIUID** de todos los proveedores de transporte activo señalados por el parámetro _lpUIDList.:_</span><span class="sxs-lookup"><span data-stu-id="71af8-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID** s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="71af8-115">Para recuperar una lista de todos los tipos de direcciones que puede controlar uno de los proveedores de transporte activo, llame a [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="71af8-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="71af8-116">**EnumAdrTypes** devuelve una matriz de cadenas que describe los tipos de direcciones admitidos por los proveedores de transporte que están activos en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="71af8-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

