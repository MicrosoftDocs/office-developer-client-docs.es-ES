---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Devuelve la marca de la cuenta de la cuenta que entrega el mensaje.
ms.openlocfilehash: ba54bffb60a05a3b4a1ff30519960740af93ebd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816306"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Devuelve la marca de la cuenta de la cuenta que entrega el mensaje.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidInetAcctStamp  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008581  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe contener el mismo valor que se devuelve desde la propiedad [PROP_ACCT_STAMP](prop_acct_stamp.md) de API de administración de cuentas para la cuenta que entrega el mensaje. 
  
Los proveedores de almacén de mensajes exponen esta propiedad con nombre y [PidLidInternetAccountName](pidlidinternetaccountname.md) para que se producen las siguientes acciones: 
  
- Cuando un usuario hace clic en **responder a todos** en un mensaje de correo electrónico, Outlook quita la dirección de correo electrónico que está asociada con la cuenta y se marca en el mensaje desde la lista de destinatarios de la respuesta. Este comportamiento se produce a menos que esta dirección de correo electrónico es el remitente del mensaje original. 
    
- De forma predeterminada, Outlook envía las respuestas y reenvía los mensajes a través de la cuenta que se marca en el mensaje original.
    
Normalmente, el Administrador de protocolos de Outlook entrega los mensajes, y Outlook establece las propiedades **PidLidInternetAccountName** y **PidLidInternetAccountStamp** para indicar la cuenta que entrega el mensaje. Sin embargo, si un almacén de mensajes se complementa con un transporte, el Administrador de protocolos de Outlook no entregar mensajes y Outlook no puede establecer estas propiedades. En este escenario, Outlook llama a la función [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) . Si desea que el proveedor de almacenamiento de mensajes exponer estas propiedades con nombre, debe implementar **IMAPIProp::GetIDsFromNames** y se devuelven etiquetas de propiedad a través del parámetro de salida *lppPropTags* . Outlook, a continuación, puede llamar al método de [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) mediante el uso de estas etiquetas de propiedad, y el proveedor de almacenamiento de mensajes puede devolver el nombre de cuenta y la marca de la cuenta deseada. 
  
Para admitir estas propiedades con nombre, los proveedores de almacén deben esperar a que Outlook use **IMAPIProp::GetIDsFromNames** para obtener la etiqueta de propiedad para esta propiedad. Outlook especifica los siguientes valores de la estructura [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) que corresponde a esta propiedad con nombre, que se pasa como parte de la matriz señalada por el parámetro de entrada *lppPropNames* de **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)
- [Propiedad canónica PidLidInternetAccountStamp](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

