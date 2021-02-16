---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Devuelve la marca de cuenta de la cuenta que entregó el mensaje.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327730"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="abfa5-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="abfa5-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="abfa5-104">Devuelve la marca de cuenta de la cuenta que entregó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="abfa5-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="abfa5-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="abfa5-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abfa5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="abfa5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abfa5-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="abfa5-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="abfa5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="abfa5-108">Property set:</span></span>  <br/> |<span data-ttu-id="abfa5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="abfa5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="abfa5-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="abfa5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abfa5-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="abfa5-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="abfa5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="abfa5-112">Data type:</span></span>  <br/> |<span data-ttu-id="abfa5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="abfa5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="abfa5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="abfa5-114">Area:</span></span>  <br/> |<span data-ttu-id="abfa5-115">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="abfa5-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abfa5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abfa5-116">Remarks</span></span>

<span data-ttu-id="abfa5-117">Esta propiedad debe contener el mismo valor que se devuelve de la propiedad API de administración de [PROP_ACCT_STAMP](prop_acct_stamp.md) para la cuenta que entregó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="abfa5-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="abfa5-118">Los proveedores de almacenamiento de mensajes exponen esta propiedad con nombre [y PidLidInternetAccountName](pidlidinternetaccountname.md) para que se produzcan las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="abfa5-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="abfa5-119">Cuando un usuario  hace clic en Responder a todos en un mensaje de correo electrónico, Outlook quita la dirección de correo electrónico asociada a la cuenta y se marca en el mensaje de la lista de destinatarios de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abfa5-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="abfa5-120">Este comportamiento se produce a menos que esta dirección de correo electrónico sea el remitente del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="abfa5-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="abfa5-121">De forma predeterminada, Outlook envía respuestas y reenvía mensajes a través de la cuenta que se marca en el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="abfa5-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="abfa5-122">Normalmente, el Administrador de protocolo de Outlook entrega mensajes y Outlook establece las propiedades **PidLidInternetAccountName** y **PidLidInternetAccountStamp** para indicar la cuenta que entregó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="abfa5-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="abfa5-123">Sin embargo, si un almacén de mensajes está estrechamente unido a un transporte, el Administrador de protocolo de Outlook no entrega mensajes y Outlook no puede establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="abfa5-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="abfa5-124">En este escenario, Outlook llama a la [función IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abfa5-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="abfa5-125">Si el proveedor del almacén de mensajes desea exponer estas propiedades con nombre, debe implementar **IMAPIProp::GetIDsFromNames** y devolver etiquetas de propiedad a través del parámetro de salida  *lppPropTags*  .</span><span class="sxs-lookup"><span data-stu-id="abfa5-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="abfa5-126">A continuación, Outlook puede llamar al método [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) mediante estas etiquetas de propiedad, y el proveedor del almacén de mensajes puede devolver el nombre de cuenta y la marca de la cuenta deseada.</span><span class="sxs-lookup"><span data-stu-id="abfa5-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="abfa5-127">Para admitir estas propiedades con nombre, los proveedores de almacenamiento deben esperar que Outlook use **IMAPIProp::GetIDsFromNames** para obtener la etiqueta de propiedad de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="abfa5-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="abfa5-128">Outlook especifica los siguientes valores para la estructura [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) que corresponde a esta propiedad con nombre, que se pasa como parte de la matriz señalada por el parámetro de entrada  *lppPropNames*  de **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="abfa5-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abfa5-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="abfa5-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="abfa5-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="abfa5-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="abfa5-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="abfa5-131">ulKind:</span></span>  <br/> |<span data-ttu-id="abfa5-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="abfa5-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="abfa5-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="abfa5-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="abfa5-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="abfa5-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abfa5-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="abfa5-135">See also</span></span>

- [<span data-ttu-id="abfa5-136">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="abfa5-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="abfa5-137">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="abfa5-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="abfa5-138">Propiedad canónica PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="abfa5-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

