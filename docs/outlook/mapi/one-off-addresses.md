---
title: Direcciones puntuales
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e6bda55951d8df5c5da272750c631ec105b2ccf2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409114"
---
# <a name="one-off-addresses"></a>Direcciones puntuales

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las direcciones de uso único se usan para enviar mensajes a destinatarios de uso único, destinatarios que no tienen una entrada correspondiente en ninguno de los contenedores de la libreta de direcciones de la sesión. Los clientes pueden crear direcciones de uso único al agregar nuevas entradas a la libreta de direcciones o a destinatarios nuevos en la lista de destinatarios de un mensaje saliente. Las direcciones de uso único pueden agregarse a cualquier contenedor que sea modificable.
  
Para crear una dirección de un solo uso, los clientes usan una plantilla especial que contiene controles de edición para introducir toda la información que constituye una dirección de uso único. Las direcciones de uso único, como las direcciones de otros tipos, usan un formato predefinido. MAPI define el formato de la dirección de un solo uso de la siguiente manera:
  
`Display name[Address type:Email address]`
  
Hay seis componentes en este formato y algunas reglas sobre la cotización de caracteres. Los componentes se describen en la tabla siguiente.
  
|**Componente**|**Uso**|**Descripción**|
|:-----|:-----|:-----|
|Nombre completo (DN)  <br/> |Opcional  <br/> |Si no está presente, **IAddrBook:: ResolveName** usa la parte visible de la dirección de correo electrónico como nombre para mostrar. Puede incluir espacios en blanco. Para obtener más información, vea [IAddrBook:: ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obligatorio  <br/> |Define el principio de la información de la dirección y el tipo.  <br/> |
|]  <br/> |Obligatorio  <br/> |Define el final de la información de tipo y dirección. Si algo que no es un espacio en blanco sigue a este carácter, la entrada no se trata como un destinatario personalizado.  <br/> |
|Tipo de dirección  <br/> |Obligatorio  <br/> |Tipo de dirección; se asigna a un formato de dirección específico. Para obtener más información, consulte [tipos de direcciones MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obligatorio  <br/> |Separa el tipo de dirección de la dirección de correo electrónico.  <br/> |
|Dirección de correo electrónico  <br/> |Obligatorio  <br/> |Direcci�n del destinatario. Puede incluir espacios en blanco.  <br/> |
   
MAPI usa conjuntos de caracteres comillas específicos para permitir que las direcciones contengan caracteres especiales como coma (,), corchete de apertura ([) y dos puntos (:) y algunos caracteres que no se pueden escribir, como el retorno de carro o el avance de línea o cualquier otro equivalente hexadecimal. El carácter de cita es la barra diagonal inversa\)(. Por lo tanto, si los clientes o proveedores deben insertar una barra diagonal inversa en una dirección, deben incluir el carácter de comillas\\("").
  
Los clientes y los proveedores de servicios pueden usar esta técnica de Comillas en cualquiera de los campos de tipo no fijos. Por ejemplo, la siguiente entrada se traduce a Bill lee como el nombre para mostrar, MSPEER como el tipo de dirección y \\billll\in como dirección de correo electrónico:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Para insertar caracteres no especificables especiales, los clientes y los proveedores de servicios utilizan un carácter de Comillas seguido de una x y dos dígitos hexadecimales para representar su equivalente hexadecimal. Por ejemplo, si una dirección tiene un carácter no interescribeble que equivale a un retorno de carro (\0d) en hexadecimal, un cliente las escribiría de la siguiente manera:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook:: ResolveName** también analiza automáticamente la mayoría de las direcciones SMTP, buscando direcciones con el siguiente formato: 
  
`XXX@YYY.ZZZ`

Aunque no todos los formatos de RFC822 posibles se controlan, este análisis automático es adecuado para la mayoría de los usuarios. **ResolveName** incluye esta funcionalidad para permitir que los usuarios escriban direcciones SMTP directamente en un mensaje y que tengan ese mensaje ir al usuario de Internet. Los componentes XXX, YYY y ZZZ de la dirección pueden tener uno o más caracteres. La arroba (@) no se puede incluir en los componentes de dirección XXX, YYY o ZZZ y el componente YYY tampoco puede incluir el punto. Como los caracteres siguientes son caracteres especiales en direcciones SMTP, MAPI convierte automáticamente un nombre para mostrar que contiene estos caracteres en una dirección de uso único: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
A todas las direcciones de uso único se les asigna un identificador de entrada único correspondiente. Para realizar esta tarea, los clientes llaman a **IAddrBook:: CreateOneOff** y los proveedores de transporte llaman a **IMAPISupport:: CreateOneOff**. Para obtener más información, vea [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) y [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). Al procesar los mensajes entrantes, los proveedores de transporte crean identificadores de entrada de un solo uso para las direcciones de puerta de enlace y para las direcciones que los proveedores de libreta de direcciones asociados con el transporte no pueden controlar. Los proveedores de transporte comprueban el tipo de cada dirección en un mensaje para determinar si un proveedor de libreta de direcciones asociado con el transporte puede controlarla. Si no es así, los proveedores de transporte llaman a **IMAPISupport:: CreateOneOff** para asociar la dirección con un identificador de entrada único. 
  
Los identificadores de entrada de un solo uso incluyen la siguiente información en el orden siguiente:
  
1. **MAPIUID**
    
2. Versión
    
3. Flags
    
4. Nombre completo (DN)
    
5. Tipo de dirección
    
6. Dirección de correo electrónico
    
En las llamadas a **IAddrBook:: CreateOneOff** y **IMAPISupport:: CreateOneOff**, los clientes y los proveedores de transporte pueden establecer una marca que indique si el destinatario representado por la dirección de uso único puede procesar texto con formato o OLE incrustado. Object. Para indicar que un destinatario puede controlar el texto con formato y los objetos OLE, los clientes y los proveedores de transporte establecen la marca MAPI_SEND_NO_RICH_INFO en el parámetro _ulFlags_ . MAPI, a continuación, establece la propiedad **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) del destinatario de un solo uso en false. Si no se establece esta marca, MAPI establece **PR_SEND_RICH_INFO** en true a menos que la dirección de uso único se interprete como una dirección SMTP. En este caso, **PR_SEND_RICH_INFO** valor predeterminado es false. 
  
## <a name="see-also"></a>Ver también

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

