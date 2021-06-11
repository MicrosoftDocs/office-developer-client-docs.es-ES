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
  
Las direcciones de uso único se usan para enviar mensajes a destinatarios únicos, destinatarios que no tienen una entrada correspondiente en ninguno de los contenedores de la libreta de direcciones de la sesión. Los clientes pueden crear direcciones únicas cuando agregan nuevas entradas a la libreta de direcciones o a nuevos destinatarios a la lista de destinatarios de un mensaje saliente. Las direcciones únicas se pueden agregar a cualquier contenedor que sea modificable.
  
Para crear una dirección única, los clientes usan una plantilla especial que contiene controles de edición para especificar toda la información que forma una dirección única. Las direcciones de uso único, como las direcciones de otros tipos, usan un formato predefinido. MAPI define el formato de dirección único de la siguiente manera:
  
`Display name[Address type:Email address]`
  
Hay seis componentes en este formato y algunas reglas sobre la cita de caracteres. Los componentes se describen en la tabla siguiente.
  
|**Componente**|**Uso**|**Descripción**|
|:-----|:-----|:-----|
|Nombre para mostrar  <br/> |Opcional  <br/> |Si no está presente, **IAddrBook::ResolveName** usa la parte visible de la dirección de correo electrónico como nombre para mostrar. Puede incluir espacios en blanco. Para obtener más información, vea [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obligatorio  <br/> |Delinea el inicio de la información de tipo y dirección.  <br/> |
|]  <br/> |Obligatorio  <br/> |Delinea el final de la información de tipo y dirección. Si algo distinto del espacio en blanco sigue este carácter, la entrada no se trata como un destinatario personalizado.  <br/> |
|Tipo de dirección  <br/> |Obligatorio  <br/> |Tipo de dirección; se asigna a un formato de dirección específico. Para obtener más información, vea [Tipos de direcciones MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obligatorio  <br/> |Separa el tipo de dirección de la dirección de correo electrónico.  <br/> |
|Dirección de correo electrónico  <br/> |Obligatorio  <br/> |Direcci�n del destinatario. Puede incluir espacios en blanco.  <br/> |
   
MAPI usa conjuntos concretos de caracteres de cita para permitir que las direcciones contengan caracteres especiales como coma (,), corchete izquierdo ([) y dos puntos (:) y algunos caracteres no tipo, como el retorno de carro o la fuente de línea o cualquier otro equivalente hexadecimal. El carácter de cita es la barra diagonal inversa ( \) . Por lo tanto, si los clientes o proveedores deben insertar una barra diagonal inversa en una dirección, deben preceirla con el carácter de cita (" \\ ").
  
Los clientes y los proveedores de servicios pueden usar esta técnica de cita en cualquiera de los campos no fijos que se pueden escribir. Por ejemplo, la siguiente entrada se traduce a Bill Lee como el nombre para mostrar, MSPEER como el tipo de dirección y \\ billll\in como la dirección de correo electrónico:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Para insertar caracteres especiales que no se pueden escribir, los clientes y los proveedores de servicios usan un carácter de cita seguido de un x y dos dígitos hexadecimales para representar su equivalente hexadecimal. Por ejemplo, si una dirección tiene un carácter no tipo que equivale a una devolución de carro (\0d) en hexadecimal, un cliente las escribiría como:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName también** analiza automáticamente la mayoría de las direcciones SMTP, buscando direcciones con el siguiente formato: 
  
`XXX@YYY.ZZZ`

Aunque no se controlan todos los formatos RFC822 posibles, este análisis automático es adecuado para la mayoría de los usuarios. **ResolveName** incluye esta funcionalidad para permitir que los usuarios escriban direcciones SMTP directamente en un mensaje y que ese mensaje vaya al usuario de Internet. Los componentes XXX, YYY y ZZZ de la dirección pueden ser uno o más caracteres. El signo at (@) no se puede incluir en los componentes de dirección XXX, YYY o ZZZ y el componente YYY tampoco puede incluir el punto. Dado que los siguientes caracteres son caracteres especiales en direcciones SMTP, MAPI convierte automáticamente un nombre para mostrar que contiene estos caracteres en una dirección única: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
A cada dirección única se le asigna un identificador de entrada único correspondiente. Para realizar esta asignación, los clientes llaman **a IAddrBook::CreateOneOff** y los proveedores de transporte llaman **a IMAPISupport::CreateOneOff**. Para obtener más información, vea [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Al procesar mensajes entrantes, los proveedores de transporte crean identificadores de entrada únicos para las direcciones de puerta de enlace y para las direcciones que los proveedores de libreta de direcciones asociados del transporte no pueden controlar. Los proveedores de transporte comprueban el tipo de cada dirección de un mensaje para determinar si puede ser manejada por un proveedor de libreta de direcciones asociado al transporte. Si no es posible, los proveedores de transporte llaman a **IMAPISupport::CreateOneOff** para asociar la dirección con un identificador de entrada único. 
  
Los identificadores de entrada únicos incluyen la siguiente información en el siguiente orden:
  
1. **MAPIUID**
    
2. Versión
    
3. Flags
    
4. Nombre para mostrar
    
5. Tipo de dirección
    
6. Dirección de correo electrónico
    
En las llamadas a **IAddrBook::CreateOneOff** e **IMAPISupport::CreateOneOff**, los clientes y los proveedores de transporte pueden establecer una marca que indica si el destinatario representado por la dirección única puede procesar texto con formato u objetos OLE incrustados. Para indicar que un destinatario puede controlar el texto con formato y los objetos OLE, los clientes y los proveedores de transporte establecen la marca MAPI_SEND_NO_RICH_INFO en el _parámetro ulFlags._ A continuación, MAPI establece la propiedad del destinatario **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE. Cuando no se establece esta marca, MAPI establece **PR_SEND_RICH_INFO** en TRUE a menos que la dirección de uso único se interprete como una dirección SMTP. En este caso, **PR_SEND_RICH_INFO** predeterminado es FALSE. 
  
## <a name="see-also"></a>Vea también

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

