---
title: Direcciones de uso único
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 504ae8dddbddb1c7049574b1bdcc575a10a62c8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570096"
---
# <a name="one-off-addresses"></a>Direcciones de uso único

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Direcciones de uso único se utilizan para enviar mensajes a los destinatarios de uso único, los destinatarios que no tienen una entrada correspondiente en cualquiera de los contenedores de la libreta de direcciones de la sesión. Los clientes pueden crear direcciones de uso único al agregar nuevas entradas a la libreta de direcciones o los destinatarios nuevo a la lista de destinatarios de un mensaje saliente. Direcciones de uso único pueden agregarse a cualquier contenedor que se puede modificar.
  
Para crear una dirección de uso único, los clientes usan una plantilla especial que contiene los controles de edición para escribir toda la información que se compone de una dirección de uso único. Direcciones de uso único, al igual que las direcciones de otros tipos, utilizan un formato predefinido. El formato de dirección de uso único se define mediante MAPI de la siguiente manera:
  
`Display name[Address type:Email address]`
  
Hay seis componentes con este formato y algunas reglas acerca de caracteres para citas. Los componentes se describen en la siguiente tabla.
  
|**Componente**|**Uso**|**Descripción**|
|:-----|:-----|:-----|
|Nombre para mostrar  <br/> |Opcional  <br/> |Si no está presente, **IAddrBook::ResolveName** utiliza la parte visible de la dirección de correo electrónico como el nombre para mostrar. Puede incluir espacios en blanco. Para obtener más información, vea [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obligatorio  <br/> |Define el inicio de la información de tipo y la dirección.  <br/> |
|]  <br/> |Obligatorio  <br/> |Indica el final de la información de tipo y la dirección. Si cualquier cosa que no sea un espacio en blanco sigue este carácter, la entrada no se trata como un destinatario personalizado.  <br/> |
|Tipo de dirección  <br/> |Obligatorio  <br/> |Tipo de dirección; se asigna a un formato de dirección específico. Para obtener más información, vea [Tipos de direcciones de MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obligatorio  <br/> |Separa el tipo de dirección de la dirección de correo electrónico.  <br/> |
|Dirección de correo electrónico  <br/> |Obligatorio  <br/> |Direcci�n del destinatario. Puede incluir espacios en blanco.  <br/> |
   
MAPI utiliza determinados conjuntos de caracteres para citas para permitir direcciones contener caracteres especiales, como la coma (,), corchete ([]), la izquierda y dos puntos (:) y algunos caracteres untypeable como el transporte devuelven o fuente o cualquier otra equivalente hexadecimal de línea. El carácter de la cita es la barra diagonal inversa (\). Por lo tanto, si los clientes o proveedores deben insertar una barra diagonal inversa en una dirección, debe incluya con el carácter de cita ("\\").
  
Los clientes y proveedores de servicios pueden usar esta técnica cotización en cualquiera de los campos de nonfixed, puede escribir. Por ejemplo, la siguiente entrada se traduce a Bill Lee como el nombre para mostrar, MSPEER como el tipo de dirección, y \\billll\in como la dirección de correo electrónico:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Para insertar caracteres especiales nontypeable, clientes y proveedores de servicios de usan un carácter de cita seguido por una x y dos dígitos hexadecimales para representar su equivalente hexadecimal. Por ejemplo, si una dirección tiene un carácter de nontypeable que equivale a un carro devolver, (\0d) en hexadecimal, un cliente podría introducir ellos como:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analiza también automáticamente la mayoría de las direcciones de SMTP, busca las direcciones con el siguiente formato: 
  
`XXX@YYY.ZZZ`

Aunque no todos los formatos de RFC822 posibles de tratamiento, este análisis automática es adecuada para la mayoría de los usuarios. **ResolveName** incluye esta funcionalidad para permitir a los usuarios escribir direcciones SMTP directamente en un mensaje y tener ese mensaje vaya al usuario de Internet. Los componentes de la dirección de XXX, YYY y ZZZ pueden ser uno o más caracteres. El signo de arroba (@) no se pueden incluir en la dirección XXX, YYY o ZZZ componentes y el componente de YYY también no pueden incluir el período. Debido a que los siguientes caracteres son caracteres especiales en las direcciones SMTP, MAPI convierte automáticamente un nombre para mostrar que contiene estos caracteres en una dirección de uso único: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Cada dirección de uso único se asigna un identificador de entrada único correspondiente. Para realizar esta asignación, los clientes **IAddrBook::CreateOneOff** y los proveedores de transporte de llamadas **IMAPISupport::CreateOneOff**. Para obtener más información, vea [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) y [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Cuando se procesa los mensajes entrantes, los proveedores de transporte crean identificadores de entrada único para las direcciones de puerta de enlace y para las direcciones que no pueden ser tratadas por los proveedores de libreta de direcciones asociada a del transporte. Los proveedores de transporte comprobación el tipo de cada dirección de un mensaje para determinar si puede ser controlado por un proveedor de la libreta de direcciones asociado con el transporte. Si no se puede, los proveedores de transporte llame a **IMAPISupport::CreateOneOff** para asociar la dirección con un identificador de entrada único. 
  
Identificadores de entrada único incluyen la siguiente información en el orden siguiente:
  
1. **MAPIUID**
    
2. Versión
    
3. Marcas
    
4. Nombre para mostrar
    
5. Tipo de dirección
    
6. Dirección de correo electrónico
    
En las llamadas a **IAddrBook::CreateOneOff** y **IMAPISupport::CreateOneOff**, los clientes y los proveedores de transporte pueden establecer una marca que indica si el destinatario representado por la dirección de uso único puede procesar con formato de texto o incrustado de OLE objetos. Para indicar que un destinatario puede controlar con formato de texto y objetos OLE, los clientes y un conjunto de proveedores de transporte el indicador MAPI_SEND_NO_RICH_INFO en el parámetro _ulFlags indicado_ . MAPI, a continuación, establece en FALSE (propiedad) **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de uso único del destinatario. Cuando no se establece este marcador, MAPI establece **PR_SEND_RICH_INFO** en TRUE, a menos que la dirección de uso único se interpreta como una dirección SMTP. En este caso, **PR_SEND_RICH_INFO** el valor predeterminado es FALSE. 
  
## <a name="see-also"></a>Recursos adicionales

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

