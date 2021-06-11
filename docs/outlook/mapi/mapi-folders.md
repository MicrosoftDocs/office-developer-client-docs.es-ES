---
title: Carpetas de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6c00dce9ec489ca2b886f3e51551ba57e9eeea33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421847"
---
# <a name="mapi-folders"></a>Carpetas de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las carpetas son objetos MAPI que sirven como unidad b�sica de organizaci�n para los mensajes. Organizados jer�rquicamente, carpetas pueden contener otras carpetas y mensajes. Carpetas que m�s f�cil localizar y trabajar con los mensajes.
  
Carpetas de implementan la interfaz de [IMAPIFolder](imapifolderimapicontainer.md) , que indirectamente hereda de la interfaz de **IUnknown** a trav�s de la [IMAPIContainer](imapicontainerimapiprop.md) y las interfaces de [IMAPIProp](imapipropiunknown.md) . Los clientes utilizan **IMAPIFolder** para crear, copiar y eliminar mensajes y carpetas, para recuperar y establecer el estado del mensaje y para activar o desactivar el indicador de lectura para un mensaje. Aunque los proveedores de almac�n de mensajes necesarios para admitir todos los m�todos en **IMAPIFolder**, algunos m�todos presentan un nivel de complejidad que los proveedores de almac�n de mensajes es posible que desee evitar. MAPI guarda alg�n trabajo de los proveedores de almac�n de mensajes mediante la implementaci�n de algunas de las funciones m�s complejas de carpeta en la interfaz de [IMAPISupport](imapisupportiunknown.md) . Por ejemplo, en lugar de implementar sus propios m�todos de copia, los proveedores de almac�n de mensajes pueden llamar a los m�todos de copia en el objeto de soporte t�cnico y obtener los mismos resultados. 
  
Hay tres tipos de carpetas:
  
- Carpetas ra�z.
    
- Carpetas gen�ricas.
    
- Carpetas de b�squeda
    
Cada almac�n de mensajes tiene al menos una carpeta ra�z. La carpeta ra�z aparece en la parte superior de la jerarqu�a y contiene los mensajes y otras carpetas. Carpetas ra�z no se pueden mover, copiar, cambiar el nombre o eliminar. Hay una sola carpeta ra�z de cada almac�n de mensajes.
  
La mayor�a de otra carpetas es gen�rica. Al igual que las carpetas ra�z, carpetas gen�ricas contienen mensajes y otras carpetas. A diferencia de las carpetas ra�z, pueden se movi�, copi�, cambiar el nombre y eliminados. Pueden crearse carpetas gen�ricas en la carpeta ra�z o en otras carpetas gen�ricos. Cuando un cliente crea una carpeta gen�rica en otra carpeta, la nueva carpeta se llama una subcarpeta o carpeta secundaria. La carpeta en la que se coloca la nueva carpeta se conoce como la carpeta principal de la nueva carpeta. Carpetas gen�ricas que tienen la misma carpeta primaria se denominan carpetas del mismo nivel. Elemento del mismo nivel y no relacionado carpetas posible o pueden que no tengan nombres �nicos, seg�n el mensaje de proveedor de almac�n. Proveedores de almac�n de mensajes que requieren las carpetas del mismo nivel que tengan nombres �nicos devuelven el valor de error MAPI_E_COLLISION cuando un cliente intenta crear dos carpetas con el mismo nombre en la misma forma primaria. 
  
Una carpeta de b�squeda contiene v�nculos a los mensajes que coinciden con un conjunto de criterios predefinidos. Dado que las carpetas de b�squeda contienen v�nculos en lugar de mensajes reales, son en efecto de s�lo lectura. No pueden contener otras carpetas ni tiene mensajes o carpetas a mover o copiar en ellos. No se tienen mensajes nuevos creados en ellas. y que ellos mismos no se va a mover, copiar o cambiar el nombre. Cuando se elimina un mensaje de una carpeta de b�squeda, se elimine realmente desde la carpeta que contiene el mensaje.
  
El tipo de carpeta se almacena **en la propiedad PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)). Cada carpeta tiene esta propiedad establecida en FOLDER_GENERIC, FOLDER_ROOT o FOLDER_SEARCH, dependiendo de su tipo.
  
Cada carpeta tiene el identificador de una entrada y una clave de registro. El identificador de **entrada, PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), lo usan clientes y proveedores de servicios para abrir la carpeta. La clave de registro, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), es un valor binario que se usa para comparar la carpeta con otras carpetas. 
  
Una carpeta tiene otras propiedades para identificar el almac�n de mensajes y carpetas relacionadas. Se requieren las siguientes propiedades:
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
Algunas carpetas **admiten la PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) que describe el tipo de operaciones que puede realizar un usuario. Por ejemplo, uno de los valores v�lidos para **PR_ACCESS** es MAPI_ACCESS_DELETE, que indica que se puede quitar la carpeta. Otra opci�n, MAPI_ACCESS_MODIFY, indica que la carpeta debe ser modificable. 
  
Para obtener una lista completa de propiedades de la carpeta requerida, vea la interfaz de [IMAPIFolder](imapifolderimapicontainer.md) . 
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

