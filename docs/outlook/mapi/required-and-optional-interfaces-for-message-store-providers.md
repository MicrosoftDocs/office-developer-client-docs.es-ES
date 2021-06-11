---
title: Interfaces obligatorias y opcionales para proveedores de almacén de mensajes
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 35b1d05d742b0d8defabf84b6dbf7d418ece0bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420923"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obligatorias y opcionales para proveedores de almacén de mensajes

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define un conjunto de interfaces relacionadas con proveedores de almacén de mensajes. Debido a la amplia variedad de características que un almacén de mensajes puede elegir implementar, algunas de estas interfaces son necesarias y otras no. En la tabla siguiente se enumeran las interfaces MAPI relacionadas con los proveedores de almacén de mensajes, se especifica si las interfaces son obligatorias u opcionales y se describe su propósito.
  
|**Interfaz**|**Estado**|**Descripción**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obligatorio  <br/> |Inicia y cierra sesión en un almacén de mensajes.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obligatorio  <br/> |Abre carpetas o mensajes, comprueba la identidad del almacén de mensajes y controla las notificaciones.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obligatorio  <br/> |Abre carpetas o mensajes, busca carpetas especiales y controla envíos de mensajes.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obligatorio  <br/> |Busca y manipula mensajes y subcarpetas.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obligatorio  <br/> |Manipula datos adjuntos y establece algunas de las propiedades de un mensaje.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Obligatorio  <br/> |Permite que otros objetos presenten colecciones de datos en varios componentes MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obligatorio  <br/> |Permite a los clientes validar el estado de un almacén de mensajes y realizar algunas tareas de configuración.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Opcional  <br/> |Accede a las propiedades de datos adjuntos del mensaje si el proveedor del almacén admite datos adjuntos de archivos.  <br/> |
|**IStorage** <br/> |Opcional  <br/> |Administra objetos de almacenamiento estructurados si el proveedor del almacén admite datos adjuntos de objetos OLE.  <br/> |
|**IStream** <br/> |Opcional  <br/> |Permite que los objetos de mensaje y datos adjuntos lean y escriban datos en secuencias de objetos.  <br/> |
|**IStreamDocfile** <br/> |Opcional  <br/> |Permite a algunos proveedores de servicios abrir un objeto de almacenamiento, como un archivo compuesto en el formato de archivo OLE 2.0.  <br/> |
   
La información básica que necesita para implementar **IMAPIFolder**, **IMessage**, **IMAPIStatus** e **IMAPITable** se documenta en los temas de referencia de estas interfaces. Esta sección contiene información adicional que está más directamente relacionada con los proveedores de almacenes de mensajes. El resto de las interfaces MAPI deben implementarse de acuerdo con la información de esta sección y en los temas de referencia adecuados. Vea la sección COM y ActiveX Object Services en el SDK de Windows para obtener más información acerca de la implementación de **IStorage,** **IStream** e **IStreamDocFile**.
  
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

