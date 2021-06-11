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
  
Los clientes crean destinatarios cuando están direccionando mensajes y cuando agregan entradas a contenedores modificables de libreta de direcciones. MAPI proporciona tres métodos para crear destinatarios:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Llama **a IAddrBook::CreateOneOff** cuando crees destinatarios que se usarán para dirigir mensajes. **CreateOneOff** crea un identificador de entrada único con formato especial que se asociará a una dirección de un tipo de dirección determinado. Para obtener más información acerca de los identificadores de entrada de un solo uso y de un solo uso, vea [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).
  
Llama **a IAddrBook::NewEntry** al crear destinatarios que se van a usar para dirigir mensajes o agregarlos a un contenedor. **NewEntry** tiene tres pares de parámetros que contienen identificadores de entrada. Estos parámetros se describen de la siguiente manera: 
  
|**Par de parámetros**|**Descripción**|
|:-----|:-----|
| _cbEidContainer_ y  _lpEidContainer_ <br/> |Identificador de entrada del contenedor en el que se debe colocar la nueva entrada.  <br/> |
| _cbEidNewEntryTpl_ y  _lpEidNewEntryTpl_ <br/> |Identificador de entrada de la plantilla que se usará para crear la nueva entrada.  <br/> |
| _lpcbEidNewEntry_ y  _lppEidNewEntry_ <br/> |Identificador de entrada de la nueva entrada.  <br/> |
   
Para crear un destinatario para un mensaje saliente, establezca  _cbEidContainer_ en cero y  _lpEidContainer_ en NULL. **NewEntry** crea un destinatario con un identificador de entrada que cumple con el formato único, el mismo tipo de destinatario que se produce mediante una llamada a **IAddrBook::CreateOneOff**. 
  
Para crear un destinatario que se va a insertar en un contenedor determinado, establezca  _lpEidContainer_ en el identificador de entrada del contenedor y  _cbEidContainer_ en el número de bytes del identificador de entrada del contenedor. 
  
Para usar una plantilla para crear un destinatario, establezca  _lpEidNewEntryTpl_ en el identificador de entrada de la plantilla que se va a usar y  _cbEidNewEntryTpl_ en el recuento de bytes de este identificador de entrada. La mayoría de los contenedores de libreta de direcciones modificables admiten una o más plantillas para crear entradas de un tipo determinado. Las plantillas únicas suelen ser cuadros de diálogo, pero no siempre. Si se escribe información en la plantilla, se genera un destinatario con una dirección con el formato correcto para el tipo. 
  
Obtenga el identificador de entrada de plantilla de:
  
- La **columna PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la tabla de uso único del contenedor, a la que se tiene acceso llamando al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor y **especificando PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) como etiqueta de propiedad y IID_IMAPITable como identificador de interfaz. 
    
- Las propiedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) y **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) de un proveedor de libreta de direcciones que contiene los identificadores de entrada para el objeto de usuario de mensajería del proveedor y las plantillas de lista de distribución. 
    
> [!NOTE]
> No confunda el identificador de entrada de una nueva plantilla de entrada con un tipo diferente de identificador de entrada denominado identificador de plantilla. Los proveedores solo usan un identificador de plantilla para mantener entradas copiadas de otros proveedores; nunca la usan los clientes y no se usa para crear nuevas entradas. 
  
Para permitir al usuario determinar el tipo de entrada que se va a crear, pase cero para  _cbEidNewEntryTpl_ y NULL para  _lpEidNewEntryTpl_. Cuando esto ocurre, **NewEntry** muestra un cuadro de diálogo común creado a partir de la tabla única de MAPI, una lista jerárquica de todas las plantillas admitidas por cada proveedor de libreta de direcciones del perfil. 
  
Cuando se ha determinado un tipo de dirección, ya sea mediante la configuración del parámetro  _lpEidNewEntryTpl_ o una selección por parte del usuario de la presentación de tabla única, **NewEntry** muestra la plantilla correspondiente mediante su tabla para mostrar. Todas las nuevas plantillas de entrada **admiten la PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) propiedad. 
  
Para que **NewEntry** devuelva el identificador de entrada de la entrada creada, pase una dirección válida para los parámetros _lpcbEidNewEntry_ y _lppEidNewEntry._ MAPI coloca el nuevo identificador de entrada en la dirección señalada por  _lppEidNewEntry_ y el número de bytes del nuevo identificador de entrada en la dirección señalada por  _lpcbEidNewEntry_.
  
Llama a [IABContainer::CreateEntry](iabcontainer-createentry.md) para crear un destinatario y guardarlo en un contenedor de libreta de direcciones determinado. Este método solo se puede usar con contenedores modificables, contenedores que tienen la marca de AB_MODIFIABLE establecida en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Los proveedores de libreta de direcciones con contenedores no modificables no admiten este método. Especifique el identificador de entrada de la plantilla para crear una entrada del tipo deseado en el _parámetro lpEntryID._ 
  
En el  _parámetro ulCreateFlags,_ especifique el tipo de comprobación de entrada duplicada necesaria y si las entradas nuevas deben reemplazar a las existentes. Si **CreateEntry** no puede crear un nuevo objeto debido a la comprobación de entrada duplicada impuesta por el proveedor, no espere que se devuelva un error o una advertencia. En estas condiciones, los proveedores devuelven un código de éxito. 
  
Si está trabajando directamente con un contenedor y conoce exactamente los tipos de direcciones que puede crear el contenedor, puede llamar a **IABContainer::CreateEntry** y pasar el identificador de entrada de la plantilla adecuada. El proveedor de libreta de direcciones establece algunas propiedades predeterminadas iniciales; puede llamar a **SetProps para** establecer otros. El usuario nunca está implicado. 
  

