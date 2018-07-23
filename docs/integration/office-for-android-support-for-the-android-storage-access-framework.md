---
title: Compatibilidad de Office para Android con el marco de acceso de almacenamiento de Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office para Android se integra con el marco de acceso de almacenamiento de Android, que permite que Office abra los archivos almacenados por otro proveedor de documentos.
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816025"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Compatibilidad de Office para Android con el marco de acceso de almacenamiento de Android

Office para Android se integra con el marco de acceso de almacenamiento de Android, que permite que Office abra los archivos almacenados por otro proveedor de documentos.
  
Android 4.4 (API nivel 19) presenta el marco de acceso de almacenamiento (SAF). El SAF permite que los usuarios busquen y abran documentos, imágenes y otros archivos en todos sus proveedores de almacenamiento de documentos preferidos. Una IU estándar permite que los usuarios busquen archivos y tengan acceso a estos de forma coherente en todos los proveedores y aplicaciones.
  
## <a name="implement-a-document-provider"></a>Implementar un proveedor de documentos

Si está desarrollando una aplicación que proporciona servicios de almacenamiento para documentos, puede hacer que sus archivos estén disponibles a través del SAF mediante la [escritura de un proveedor de documentos personalizado](https://developer.android.com/guide/topics/providers/document-provider.html). Las aplicaciones de Office pueden invocar el propósito [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) o [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) para recibir los archivos devueltos por el proveedor de documentos. Tenga en cuenta que el propósito puede incluir filtros para ajustar más los criterios. 
  
## <a name="enable-free-consumer-edits"></a>Habilitar modificaciones gratuitas para consumidores

Los usuarios pueden iniciar sesión en las aplicaciones de Office con una cuenta gratuita de Microsoft para crear o editar los documentos que se almacenan en un servicio de almacenamiento orientado al consumidor. En la siguiente tabla se enumeran las propiedades obligatorias que los proveedores deben proporcionar como parte del cursor para poder habilitar la modificación gratuita para clientes de los documentos que tienen acceso mediante el marco de acceso de almacenamiento.
  
|**Propiedad**|**Índice**|**Valor**|
|:-----|:-----|:-----|
|Tipo de documento  <br/> |com_microsoft_office_doctype  <br/> |\<consumidor\>  <br/> |
|Nombre descriptivo del servicio  <br/> |com_microsoft_office_servicename  <br/> |Cualquier nombre descriptivo para el servicio, que se use para identificar un documento en la lista de elementos recientes en las aplicaciones de Office. Tenga en cuenta que se debe proporcionar la propiedad "Contrato de condiciones de uso" para que se pueda mostrar el nombre descriptivo del servicio.  <br/> |
|Contrato de condiciones de uso  <br/> |com_microsoft_office_termsofuse  <br/> |\<Acepto los términos ubicados en http://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Integración con Office](integrate-with-office.md)
    
- [Conceptos básicos sobre el proveedor de contenido](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [Creación de un proveedor de contenido](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Guía para desarrolladores del marco de acceso de almacenamiento](https://developer.android.com/guide/topics/providers/document-provider.html)
    

