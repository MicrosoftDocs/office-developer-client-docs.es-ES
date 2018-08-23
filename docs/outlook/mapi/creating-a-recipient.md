---
title: Crear un destinatario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4d4777077dae5effed9f233dd020628ee0dcfed5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578048"
---
# <a name="creating-a-recipient"></a>Crear un destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes creación a destinatarios cuando dirigir los mensajes y cuando se agregan entradas a contenedores de la libreta de direcciones modificable. MAPI proporciona tres métodos para la creación de destinatarios:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Llamar a **IAddrBook::CreateOneOff** cuando esté creando los destinatarios que se usará para los mensajes de la dirección. **CreateOneOff** crea un identificador de entrada único con formato especial para asociarse con una dirección de un tipo de dirección concreto. Para obtener más información acerca de uso único y los identificadores de entrada único, vea [Direcciones de uso único](one-off-addresses.md) y los [Identificadores de entrada de uso único](one-off-entry-identifiers.md).
  
Llamada **IAddrBook::NewEntry** cuando esté creando los destinatarios se utiliza para dirigir mensajes o para agregar a un contenedor. **NewEntry** tiene tres pares de parámetros que contienen los identificadores de entrada. Estos parámetros se describen de la siguiente manera: 
  
|**Par de parámetro**|**Descripción**|
|:-----|:-----|
| _cbEidContainer_ y _lpEidContainer_ <br/> |Identificador de entrada para el contenedor en el que se debe colocar la nueva entrada.  <br/> |
| _cbEidNewEntryTpl_ y _lpEidNewEntryTpl_ <br/> |Identificador de entrada de la plantilla que se usará para crear la nueva entrada.  <br/> |
| _lpcbEidNewEntry_ y _lppEidNewEntry_ <br/> |Identificador de entrada para la nueva entrada.  <br/> |
   
Para crear a un destinatario de un mensaje saliente, establezca _cbEidContainer_ en cero y _lpEidContainer_ en NULL. **NewEntry** crea a un destinatario con un identificador de entrada que se ajusta al formato de uso único, el mismo tipo de destinatario que se produce en una llamada a **IAddrBook::CreateOneOff**. 
  
Para crear un destinatario que se insertará en un contenedor determinado, establezca _lpEidContainer_ en el contenedor identificador de entrada y _cbEidContainer_ para el número de bytes en el identificador de entrada del contenedor. 
  
Para usar una plantilla para crear a un destinatario, establezca _lpEidNewEntryTpl_ en el identificador de entrada de la plantilla que se usará y _cbEidNewEntryTpl_ que el recuento de bytes en este identificador de entrada. Más contenedores modificable de la libreta de direcciones compatible con una o varias plantillas para la creación de entradas de un tipo determinado. Plantillas de uso único suelen ser, pero no siempre, cuadros de diálogo. Introducir la información en la plantilla genera a un destinatario con una dirección que tiene el formato correcto para el tipo. 
  
Obtener el identificador de entrada de plantilla desde cualquiera:
  
- La columna de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) en la tabla de uso único del contenedor, tener acceso a llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor y especificando **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) como la etiqueta de propiedad y IID_IMAPITable como el identificador de interfaz. 
    
- Una libreta de direcciones **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) del proveedor y propiedades de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) que contiene los identificadores de entrada para el proveedor de mensajería de objeto de usuario y plantillas de lista de distribución. 
    
> [!NOTE]
> Es importante no confundir el identificador de entrada de una nueva entrada de la plantilla con un tipo de identificador de entrada denominado un identificador de plantilla diferente. Un identificador de plantilla se utiliza sólo por los proveedores para mantener las entradas que se copió desde otros proveedores; nunca se usa por los clientes y no se usa para crear nuevas entradas. 
  
Para habilitar el usuario determinar el tipo de entrada que se creará, pase NULL para _lpEidNewEntryTpl_y cero para _cbEidNewEntryTpl_ . Cuando esto ocurre, **NewEntry** muestra un cuadro de diálogo común creado a partir de la tabla de uso único de MAPI: una lista jerárquica de todas las plantillas compatibles con cada proveedor de libreta de direcciones en el perfil. 
  
Cuando un tipo de dirección se ha determinado, ya sea a través de la configuración del parámetro _lpEidNewEntryTpl_ o una selección por el usuario de la visualización de la tabla de uso único, **NewEntry** muestra la plantilla correspondiente con su tabla para mostrar. Todas las nuevas plantillas de entrada admiten la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Para que **NewEntry** devolver el identificador de entrada de la entrada creada, pase una dirección válida para los parámetros _lpcbEidNewEntry_ y _lppEidNewEntry_ . MAPI coloca el nuevo identificador de entrada en la dirección indicada por _lppEidNewEntry_ y el número de bytes del identificador de entrada nueva en la dirección indicada por _lpcbEidNewEntry_.
  
Llame a [IABContainer::CreateEntry](iabcontainer-createentry.md) para crear a un destinatario y vuelva a guardarla en un contenedor de la libreta de direcciones determinada. Puede utilizar este método sólo con contenedores modificables: contenedores que tienen la AB_MODIFIABLE marcador establecido en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Los proveedores de la libreta de direcciones con contenedores no modificables no admiten este método. Especifique el identificador de entrada de la plantilla para la creación de una entrada del tipo que desee en el parámetro _lpEntryID_ . 
  
En el parámetro _ulCreateFlags_ , especifique el tipo de entrada duplicada comprobación necesarios y si las nuevas entradas deberían reemplazar los existentes. Si se produce un error en **CreateEntry** crear un nuevo objeto debido a la comprobación de entrada duplicada impuestas por el proveedor, no debe esperar ver un error o advertencia devuelto. En estas condiciones, proveedores de devuelven un código correcto. 
  
Si está trabajando directamente con un contenedor y sabe exactamente los tipos de direcciones que se puede crear el contenedor, puede llamar a **IABContainer::CreateEntry** y pase el identificador de entrada para la plantilla adecuada. El proveedor de la libreta de direcciones establece algunas propiedades inicial predeterminada; se puede llamar a **SetProps** para establecer otras personas. El usuario nunca está ocupado. 
  

