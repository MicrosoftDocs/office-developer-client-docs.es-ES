---
title: Interfaces obligatorias y opcionales para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: d8cd03fa184865446da48d7532764ba71e0e47d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820500"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obligatorias y opcionales para proveedores de almacenamiento de mensajes

 
  
**Hace referencia a**: Outlook 
  
MAPI define un conjunto de interfaces que se relacionan con los proveedores de almacén de mensajes. Debido a la amplia gama de características que puede elegir un almacén de mensajes para implementar, algunas de estas interfaces son necesarios y otros no. En la siguiente tabla se enumeran las interfaces MAPI que están relacionadas con los proveedores de almacén de mensajes, especifica si las interfaces son obligatorios u opcionales y describe su propósito.
  
|**Interfaz**|**Status**|**Descripción**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obligatorio  <br/> |Registros en y cerrar un almacén de mensajes.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obligatorio  <br/> |Abre las carpetas o mensajes, comprueba la identidad del almacén de mensajes y controla las notificaciones.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obligatorio  <br/> |Abre las carpetas o mensajes, busca carpetas especiales y administra los envíos de mensajes.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obligatorio  <br/> |Busca y manipula los mensajes y subcarpetas.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obligatorio  <br/> |Manipula los datos adjuntos y se establecen algunas de las propiedades de un mensaje.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Obligatorio  <br/> |Permite a los otros objetos presentar las colecciones de datos a diversos componentes MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obligatorio  <br/> |Permite a los clientes para validar el estado de un almacén de mensajes y para llevar a cabo algunas tareas de configuración.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Opcional  <br/> |Tiene acceso a propiedades de datos adjuntos del mensaje si el proveedor de almacenamiento es compatible con archivos adjuntos.  <br/> |
|**IStorage** <br/> |Opcional  <br/> |Administra los objetos de almacenamiento estructurado si el proveedor de almacenamiento es compatible con datos adjuntos de objeto OLE.  <br/> |
|**IStream** <br/> |Opcional  <br/> |Permite a los objetos de mensaje y datos adjuntos leer y escribir datos en objetos stream.  <br/> |
|**IStreamDocfile** <br/> |Opcional  <br/> |Permite que algunos proveedores de servicios abrir un objeto de almacenamiento, como un archivo compuesto en el formato de archivo OLE 2.0.  <br/> |
   
La información básica que necesita implementar **IMAPIFolder**, **IMessage**, **IMAPIStatus**y **IMAPITable** se documenta en los temas de referencia para estas interfaces. Esta sección contiene información adicional que está más directamente relacionada con los proveedores de almacén de mensajes. Según la información de esta sección y en los temas de referencia adecuado, se debe implementar el resto de las interfaces MAPI. Vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows para obtener más información acerca de cómo implementar **IStorage**, **IStream**y **IStreamDocFile**.
  
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

