---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425900"
---
# <a name="adrparm"></a>ADRPARM

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la presentación y el comportamiento del cuadro de diálogo de direcciones comunes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Miembros

**cbABContEntryID**
  
> Recuento de bytes en el identificador de entrada al que **apunta lpABContEntryID**.
    
**lpABContEntryID**
  
> Puntero al identificador de entrada del contenedor que proporciona la lista inicial de direcciones de destinatario que se muestran en el cuadro de diálogo de dirección.
    
**ulFlags**
  
> Máscara de bits de marcas asociadas a varias opciones del cuadro de diálogo de direcciones. Se pueden establecer las siguientes marcas:
    
AB_RESOLVE
  
> Habilite todos los nombres para que se resuelvan después de cerrar el cuadro de diálogo de dirección. Si hay entradas ambiguas que resultan del proceso de resolución de nombres, aparece un cuadro de diálogo para solicitar ayuda al usuario para resolverlas. Al establecer esta marca se garantiza que se resuelvan todos los nombres devueltos por [IAddrBook::Address.](iaddrbook-address.md) 
    
AB_SELECTONLY
  
> Deshabilitar la creación de direcciones de uso único para una lista de destinatarios. Esta marca solo se usa si el cuadro de diálogo es modal, tal como lo indica el DIALOG_MODAL marca que se va a establecer.
    
ADDRESS_ONE
  
> El usuario puede seleccionar exactamente un destinatario en lugar de varios destinatarios de una lista. Esta marca solo es válida cuando **cDestFields** es cero y el cuadro de diálogo es modal, como se indica en el DIALOG_MODAL marca que se va a establecer. 
    
DIALOG_MODAL
  
> Hace que se muestre la versión modal del cuadro de diálogo dirección común. Esta marca o DIALOG_SDI deben establecerse; no se pueden establecer ambos. 
    
DIALOG_OPTIONS
  
> Hace que **el botón Opciones** de envío se muestre en el cuadro de diálogo. Esta marca solo se usa si el cuadro de diálogo es modal, tal como lo indica el DIALOG_MODAL marca que se va a establecer. 
    
DIALOG_SDI
  
> Hace que se muestre la versión no modelada del cuadro de diálogo de dirección común. Esta marca o DIALOG_MODAL debe establecerse; no se pueden establecer ambos. El DIALOG_SDI se omite para los clientes que no son de Outlook y se mostrará la versión modal del cuadro de diálogo. Por lo tanto, no debe esperarse un puntero a un controlador en el parámetro  _lpulUIParam_ de [IAddrBook::Address](iaddrbook-address.md).
    
**lpReserved**
  
> Reservado, debe ser cero.
    
**ulHelpContext**
  
> Especifica el contexto de la **Ayuda que** se mostrará primero cuando el usuario haga clic en el botón Ayuda en el cuadro de diálogo de dirección. 
    
**lpszHelpFileName**
  
> Puntero al nombre de un archivo de Ayuda que se asociará con el cuadro de diálogo de dirección. El **miembro lpszHelpFileName** se usa junto con **ulHelpContext** para llamar a la función **WinHelp de** Windows. 
    
**lpfnABSDI**
  
> Puntero a una función MAPI basada en el prototipo [ACCELERATEABSDI](accelerateabsdi.md) o NULL. Este miembro se aplica solo a la versión no modelada del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se está configurando. Los clientes que están creando una estructura **ADRPARM** para pasar a [IAddrBook::Address](iaddrbook-address.md) siempre deben establecer el miembro **lpfnABSDI** en NULL. Si se DIALOG_SDI marca, MAPI la establecerá en una función válida antes de devolverla. Los clientes llaman a esta función desde su bucle de mensajes para asegurarse de que los aceleradores del cuadro de diálogo de la libreta de direcciones funcionan. Cuando se descarta el cuadro de diálogo y MAPI llama a la función a la que apunta el miembro **lpfnDismiss,** los clientes deben desenlazchar la función **ACCELERATEABSDI** de su bucle de mensaje. 
    
**lpfnDismiss**
  
> Puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL. Este miembro solo se aplica a la versión no modelada del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo de dirección no modelada e informa a un cliente que llama a **IAddrBook::Address** de que el cuadro de diálogo ya no está activo. 
    
**lpvDismissContext**
  
> Puntero a la información de contexto que se pasará a la **función DISMISSMODELESS** a la que apunta el **miembro lpfnDismiss.** Este miembro se aplica solo a la versión no modelada del cuadro de diálogo, como se indica en la DIALOG_SDI marca que se está configurando. 
    
**lpszCaption**
  
> Puntero al texto que se usará como título del cuadro de diálogo dirección común.
    
**lpszNewEntryTitle**
  
> Puntero al texto que se usará como etiqueta de  botón para el botón que invoca el cuadro de diálogo Nueva entrada u otro cuadro de diálogo. 
    
**lpszDestModesTitle**
  
> Puntero al texto que se usará como título para los controles de cuadro de texto del destinatario que pueden aparecer en la versión modal del cuadro de diálogo de dirección común. Este miembro no se usa para cuadros de diálogo sin modelo. 
    
**cDestFields**
  
> Número de controles de cuadro de texto del destinatario en la versión modal del cuadro de diálogo de dirección, o cero si el cuadro de diálogo es no modal. El cuadro de diálogo de dirección está abierto para explorar únicamente cuando se cumplen las siguientes condiciones: 
    
  - El **miembro cDestFields** se establece en cero. 
    
  - Se DIALOG_BOX marca de configuración.
    
  - La ADDRESS_ONE no está establecida.
    
  Establecer **cDestFields en** 0XFFFFFFFF implica que MAPI debe crear el número predeterminado de controles de cuadro de texto de destinatario. En este caso, los **miembros lppszDestTitles** **e lpulDestComps** deben ser NULL. 
    
**nDestFieldFocus**
  
> Indica el control de cuadro de texto concreto que debe tener el foco inicial cuando aparece la versión modal del cuadro de diálogo. Este valor debe estar entre 0 y el valor de **cDestFields** menos 1. 
    
**lppszDestTitles**
  
> Puntero a una matriz de etiquetas para botones asociados con cada uno de los controles de cuadro de texto que se muestran en la versión modal del cuadro de diálogo de dirección. El valor del miembro **cDestFields** indica el número de etiquetas incluidas en la matriz. Si el **miembro lppszDestTitles** es NULL, el **método Address** usa títulos predeterminados. 
    
**lpulDestComps**
  
> Puntero a una matriz de valores de tipo de destinatario, como MAPI_TO, MAPI_CC y MAPI_BCC, asociados con cada control de cuadro de texto. El valor del miembro **CDestFields** indica el número de tipos de destinatarios incluidos en la matriz. Los valores a los que **apunta lpulDestComps** se pueden usar para establecer la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatario. Si el **miembro lpulDestComps** es NULL, el **método Address** usa tipos de destinatarios predeterminados. 
    
**lpContRestriction**
  
> Puntero a una [estructura SRestriction](srestriction.md) que limita el tipo de entradas de dirección que se pueden mostrar en el cuadro de diálogo. 
    
**lpHierRestriction**
  
> Puntero a una **estructura SRestriction** que limita los contenedores de la libreta de direcciones que pueden proporcionar entradas de dirección que se mostrarán en el cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios usan las estructuras **ADRPARM** para controlar la apariencia y el comportamiento de los cuadros de diálogo de direcciones comunes mapi. Hay dos variedades del cuadro de diálogo de dirección: no modal y modal. Algunos de los miembros de la estructura **ADRPARM** se aplican a ambas versiones del cuadro de diálogo, pero algunos solo se aplican a una de las dos versiones. En la tabla siguiente se relacionan los miembros de una estructura **ADRPARM** con su uso con los cuadros de diálogo de direcciones comunes. 
  
|Miembro ADRPARM|Tipo de cuadro de diálogo|
|:-----|:-----|
|**cbABContEntryID** y **lpABContEntryID** <br/> |Modal y no modal  <br/> |
|**ulFlags** <br/> |Modal y no modal  <br/> |
|**lpReserved** <br/> |Modal y no modal  <br/> |
|**ulHelpContext** y **lpszHelpFileName** <br/> |Modal y no modal  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss** e **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |Modal y no modal  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestFocussTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** y **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal y no modal  <br/> |
|**lpHierRestriction** <br/> |Modal y no modal  <br/> |
   
El cuadro de diálogo sin modelo es una presentación de solo lectura de entradas de uno o más contenedores de libreta de direcciones. El cuadro de diálogo puede mostrar todas las entradas de los contenedores seleccionados o limitarse solo a aquellas entradas y contenedores que coincidan con los criterios establecidos por una restricción. La restricción de contenido que apunta **lpContRestriction** puede limitar los tipos de entradas mostradas y la restricción de jerarquía que apunta **lpHierRestriction** puede limitar los contenedores que proporcionan las entradas. Para informar al autor de la llamada cuando se descarta el cuadro de diálogo, MAPI invoca una función proporcionada por el llamador que coincide con el prototipo [DISMISSMODELESS.](dismissmodeless.md) Mapi proporciona otra función, que coincide con el prototipo [ACCELERATEABSDI,](accelerateabsdi.md) y la invoca el autor de la llamada en el bucle de mensajes de Windows para facilitar el funcionamiento de los métodos abreviados de teclado. La versión modelada del cuadro de diálogo de dirección MAPI se puede mostrar cuando los clientes llaman a [IAddrBook::Address](iaddrbook-address.md) o cuando los proveedores de servicios llaman a [IMAPISupport::Address](imapisupport-address.md). 
  
El cuadro de diálogo modal es una presentación de lectura y escritura de entradas de uno o más contenedores. Su contenido puede verse afectado de la misma manera que la versión modelada por las restricciones establecidas en los miembros **lpContRestriction** y **lpHierRestriction.** Además del cuadro de lista que muestra las entradas de contenedor, el cuadro de diálogo modal puede contener entre uno y tres controles de cuadro de texto para contener las entradas seleccionadas por el usuario. Cada control de edición está asociado a un tipo de destinatario determinado o a **PR_RECIPIENT_TYPE** propiedad, como MAPI_TO. El cuadro de diálogo de dirección modal  se puede mostrar mediante cualquiera de los métodos de dirección o cuando los clientes llaman a [IAddrBook::D etails](iaddrbook-details.md) y proveedores de servicios llaman a [IMAPISupport::D etails](imapisupport-details.md). 
  
Esta ilustración incluye dos controles de cuadro de texto porque el miembro **cDestFields** de la estructura **ADRPARM** que controla la presentación de este cuadro de diálogo está establecido en 2. El primer control tiene el foco inicial porque el **miembro nDestFieldFocus** está establecido en 0. 
  
El **miembro lpszNewEntryTitle** apunta al texto de una etiqueta de botón que, cuando se selecciona, hace que se muestre un cuadro de diálogo adicional. Normalmente, como se muestra en la ilustración del cuadro de diálogo modal, el botón se etiqueta **Nuevo** y el cuadro de diálogo que aparece enumera todos los tipos de direcciones que puede crear cualquiera de los proveedores de libretas de direcciones en el perfil. Los clientes  hacen que este cuadro de diálogo Nueva entrada se muestre llamando a [IAddrBook::NewEntry](iaddrbook-newentry.md) y pasando cero para el parámetro _cbEidNewEntryTpl_ y NULL para el parámetro _lpEidNewEntryTpl_ cuando el usuario selecciona el botón. La información que se incluye en este cuadro de diálogo proviene de la tabla de uso único mapi. 
  
Cada entrada de este cuadro de diálogo está asociada a una plantilla para escribir los datos necesarios para crear una dirección del tipo en particular. La mayoría de los proveedores de libretas de direcciones suministran una plantilla para cada tipo de entrada de dirección que pueden crear. Cuando un usuario realiza una selección en este cuadro de diálogo, MAPI muestra la plantilla correspondiente.
  
Los cuatro bits más significativos del miembro **ulFlags** de la estructura **ADRPARM** contienen un número de versión que identifica la versión de la estructura **ADRPARM.** La versión actual es 0 (cero) o ADRPARM_HELP_CTX. Se producirá un error en la implementación actual de MAPI para cualquier versión de la estructura que no sea cero. 
  
Las versiones futuras de la estructura pueden ser completamente diferentes; es posible que no admitan la estructura de versión cero. Se proporcionan las siguientes macros para extraer el número de versión del miembro **ulFlags** y para combinarlo con las marcas definidas: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Consulte también

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

