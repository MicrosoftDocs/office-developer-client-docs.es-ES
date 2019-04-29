---
title: Creación de un destinatario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429589"
---
# <a name="creating-a-recipient"></a>Creación de un destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes crean destinatarios cuando se dirigen mensajes y cuando agregan entradas a contenedores de libretas de direcciones modificables. MAPI proporciona tres métodos para crear destinatarios:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Llame a **IAddrBook:: CreateOneOff** al crear destinatarios que se usarán para dirigir mensajes. **CreateOneOff** crea un identificador de entrada de un solo uso con un formato especial que se debe asociar con una dirección de un tipo de dirección determinado. Para obtener más información acerca de los identificadores de entrada de una sola desventajas y de un solo uso, vea [direcciones de uso único](one-off-addresses.md) y [identificadores de entrada de un solo uso](one-off-entry-identifiers.md).
  
Llame a **IAddrBook:: NEWENTRY** al crear destinatarios que se usarán para dirigir mensajes o para agregar a un contenedor. **NEWENTRY** tiene tres pares de parámetros que contienen identificadores de entrada. Estos parámetros se describen de la siguiente manera: 
  
|**Par de parámetros**|**Descripción**|
|:-----|:-----|
| _cbEidContainer_ y _lpEidContainer_ <br/> |Identificador de entrada del contenedor en el que se debe colocar la nueva entrada.  <br/> |
| _cbEidNewEntryTpl_ y _lpEidNewEntryTpl_ <br/> |Identificador de entrada de la plantilla que se va a usar para crear la nueva entrada.  <br/> |
| _lpcbEidNewEntry_ y _lppEidNewEntry_ <br/> |Identificador de entrada de la nueva entrada.  <br/> |
   
Para crear un destinatario para un mensaje saliente, establezca _cbEidContainer_ en cero y _lpEidContainer_ en NULL. **NEWENTRY** crea un destinatario con un identificador de entrada que se ajusta al formato único, el mismo tipo de destinatario que se produce mediante una llamada a **IAddrBook:: CreateOneOff**. 
  
Para crear un destinatario que se va a insertar en un contenedor en particular, establezca _lpEidContainer_ en el identificador de entrada del contenedor y _cbEidContainer_ en el número de bytes del identificador de entrada del contenedor. 
  
Para usar una plantilla para crear un destinatario, establezca _lpEidNewEntryTpl_ en el identificador de entrada de la plantilla que se va a usar y _cbEidNewEntryTpl_ en el número de bytes de este identificador de entrada. La mayoría de los contenedores de libretas de direcciones modificables admiten una o más plantillas para crear entradas de un tipo determinado. Los cuadros de diálogo suelen tener plantillas de uso único, pero no siempre. Al escribir información en la plantilla, se genera un destinatario con una dirección con el formato correcto para el tipo. 
  
Obtenga el identificador de entrada de plantilla de cualquiera de las siguientes opciones:
  
- La **** columna 1 ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla única del contenedor, a la que se tiene acceso llamando al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor y especificando **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) como la etiqueta de propiedad y IID_IMAPITable como identificador de interfaz. 
    
- Las propiedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) de un proveedor de libreta de direcciones que contienen los identificadores de entrada para el objeto de usuario de mensajería del proveedor y plantillas de listas de distribución. 
    
> [!NOTE]
> No confunda el identificador de entrada de una nueva plantilla de entrada con un tipo de identificador de entrada diferente denominado identificador de la plantilla. Un identificador de plantilla solo se usa por los proveedores para mantener las entradas copiadas de otros proveedores; nunca la usan los clientes y no se usa para crear nuevas entradas. 
  
Para permitir que el usuario determine el tipo de entrada que se va a crear, pase cero para _cbEidNewEntryTpl_ y null para _lpEidNewEntryTpl_. Cuando esto ocurre, **NEWENTRY** muestra un cuadro de diálogo común creado a partir de una tabla única de MAPI: una lista jerárquica de todas las plantillas que admite cada proveedor de la libreta de direcciones en el perfil. 
  
Cuando se ha determinado un tipo de dirección, ya sea a través de la configuración del parámetro _lpEidNewEntryTpl_ o de una selección realizada por el usuario desde la presentación de la tabla de uso único, **NEWENTRY** muestra la plantilla correspondiente mediante su tabla de visualización. Todas las nuevas plantillas de entrada admiten la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Para que **NEWENTRY** devuelva el identificador de entrada de la entrada creada, pase una dirección válida para los parámetros _lpcbEidNewEntry_ y _lppEidNewEntry_ . MAPI coloca el nuevo identificador de entrada en la dirección a la que apunta _lppEidNewEntry_ y el número de bytes del nuevo identificador de entrada en la dirección a la que apunta _lpcbEidNewEntry_.
  
Llame a [IABContainer:: CreateEntry](iabcontainer-createentry.md) para crear un destinatario y guardarlo en un contenedor de libreta de direcciones en particular. Solo puede usar este método con contenedores modificables: contenedores que tienen la marca AB_MODIFIABLE establecida en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Los proveedores de libretas de direcciones con contenedores no modificables no admiten este método. Especifique el identificador de entrada de la plantilla para crear una entrada del tipo deseado en el parámetro _lpEntryID_ . 
  
En el parámetro _ulCreateFlags_ , especifique el tipo de comprobación de entrada duplicada necesario y si las entradas nuevas deben reemplazar a las existentes. Si **CreateEntry** no puede crear un objeto nuevo debido a la comprobación de entrada duplicada impuesta por el proveedor, no espera que se devuelva un error o advertencia. En estas condiciones, los proveedores devuelven un código de éxito. 
  
Si trabaja directamente con un contenedor y conoce exactamente los tipos de direcciones que puede crear el contenedor, puede llamar a **IABContainer:: CreateEntry** y pasar el identificador de entrada de la plantilla correspondiente. El proveedor de la libreta de direcciones establece algunas propiedades predeterminadas iniciales; puede llamar a **SetProps** para establecer otras. El usuario nunca está implicado. 
  

