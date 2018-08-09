---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818414"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Hace referencia a**: Outlook 
  
Especifica si Microsoft Office Outlook debe examinar las carpetas de contactos en un almacén.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Tener acceso a ella:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Tipo de acceso:  <br/> |Sólo lectura o lectura y escritura según el proveedor de almacenamiento  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta. Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "NoFolderScan"  <br/> |
   
Esta propiedad proporciona una manera para los proveedores de almacén especificar a Outlook no para examinar las carpetas de contactos en el almacén para evitar la degradación del rendimiento. Se utiliza en las operaciones de combinación de correspondencia durante el cual Outlook comprueba la presencia y el valor de esta propiedad antes de iniciar el análisis.
  
De forma predeterminada, esta propiedad no se expone en un repositorio, lo que significa que Outlook puede examinar la carpeta de contactos en el almacén. Si la propiedad se expone, los valores posibles son los siguientes:
  
- Cero (0): Outlook puede llevar a cabo el examen.
    
- Valor distinto de cero: Outlook no debe examinar las carpetas de contactos en el almacén.
    

