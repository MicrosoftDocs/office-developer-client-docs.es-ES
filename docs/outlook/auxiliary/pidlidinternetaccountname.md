---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Devuelve el nombre para mostrar de la cuenta que entregó el mensaje.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327688"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Devuelve el nombre para mostrar de la cuenta que entregó el mensaje.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidInetAcctName  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008580  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe contener el mismo valor que se devuelve de la propiedad API de administración de [PROP_ACCT_NAME](prop_acct_name.md) para la cuenta que entregó el mensaje. 
  
Los proveedores de almacenamiento de mensajes exponen esta propiedad con nombre [y PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) para que se produzcan las siguientes acciones: 
  
- Cuando un usuario  hace clic en Responder a todos en un mensaje de correo electrónico, Outlook quita la dirección de correo electrónico asociada a la cuenta y se marca en el mensaje de la lista de destinatarios de la respuesta. Este comportamiento se produce a menos que esta dirección de correo electrónico sea el remitente del mensaje original. 
    
- De forma predeterminada, Outlook envía respuestas y reenvía mensajes a través de la cuenta que se marca en el mensaje original.
    
Normalmente, el Administrador de protocolo de Outlook entrega mensajes y Outlook establece las propiedades **PidLidInternetAccountName** y **PidLidInternetAccountStamp** para indicar la cuenta que entregó el mensaje. Sin embargo, si un almacén de mensajes está estrechamente unido a un transporte, el Administrador de protocolo de Outlook no entrega mensajes y Outlook no puede establecer estas propiedades. En este escenario, Outlook llama a la [función IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) Si el proveedor del almacén de mensajes desea exponer estas propiedades con nombre, debe implementar **IMAPIProp::GetIDsFromNames** y devolver etiquetas de propiedad a través del parámetro de salida  *lppPropTags*  . A continuación, Outlook puede llamar al método [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) mediante estas etiquetas de propiedad, y el proveedor del almacén de mensajes puede devolver el nombre de cuenta y la marca de la cuenta deseada. 
  
Para admitir estas propiedades con nombre, los proveedores de almacén deben esperar que Outlook use **IMAPIProp::GetIDsFromNames** para obtener la etiqueta de propiedad de esta propiedad. Outlook especifica los siguientes valores para la estructura [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) que corresponde a esta propiedad con nombre, que se pasa como parte de la matriz señalada por el parámetro de entrada  *lppPropNames*  de **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)
- [Propiedad canónica PidLidInternetAccountName](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

