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
  
Describe la presentación y el comportamiento del cuadro de diálogo Dirección común. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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

## <a name="members"></a>Members

**cbABContEntryID**
  
> Número de bytes en el identificador de entrada al que apunta **lpABContEntryID**.
    
**lpABContEntryID**
  
> Puntero al identificador de entrada del contenedor que proporciona la lista inicial de direcciones de destinatario que se muestran en el cuadro de diálogo Dirección.
    
**ulFlags**
  
> Máscara de direcciones de marcas asociadas con varias opciones del cuadro de diálogo Dirección. Se pueden establecer los siguientes indicadores:
    
AB_RESOLVE
  
> Habilitar la resolución de todos los nombres después de cerrar el cuadro de diálogo Dirección. Si hay entradas ambiguas como resultado del proceso de resolución de nombres, aparece un cuadro de diálogo para pedir ayuda al usuario que las resuelva. Si se establece este indicador se garantiza que se resuelvan todos los nombres devueltos por [IAddrBook:: Address](iaddrbook-address.md) . 
    
AB_SELECTONLY
  
> DesHabilitar la creación de direcciones de uso único para una lista de destinatarios. Esta marca solo se usa si el cuadro de diálogo es modal, tal como indica la marca DIALOG_MODAL que se va a establecer.
    
ADDRESS_ONE
  
> El usuario puede seleccionar exactamente un destinatario en lugar de varios destinatarios de una lista. Esta marca solo es válida cuando **cDestFields** es cero y el cuadro de diálogo es modal, tal como indica la marca DIALOG_MODAL que se va a establecer. 
    
DIALOG_MODAL
  
> Hace que se muestre la versión modal del cuadro de diálogo Dirección común. Se debe establecer esta marca o DIALOG_SDI; no se pueden establecer a la vez. 
    
DIALOG_OPTIONS
  
> Hace que se muestre el botón **Opciones de envío** en el cuadro de diálogo. Esta marca solo se usa si el cuadro de diálogo es modal, tal como indica la marca DIALOG_MODAL que se va a establecer. 
    
DIALOG_SDI
  
> Hace que se muestre la versión no modal del cuadro de diálogo Dirección común. Se debe establecer esta marca o DIALOG_MODAL; no se pueden establecer a la vez. La marca DIALOG_SDI se ignora para los clientes que no son de Outlook y se muestra la versión modal del cuadro de diálogo. Por lo tanto, no debe esperarse un puntero a un controlador en el parámetro _lpulUIParam_ de [IAddrBook:: Address](iaddrbook-address.md).
    
**lpReserved**
  
> Reserved, debe ser cero.
    
**ulHelpContext**
  
> Especifica el contexto de la **ayuda** que se mostrará primero cuando el usuario haga clic en el botón ayuda en el cuadro de diálogo Dirección. 
    
**lpszHelpFileName**
  
> Puntero al nombre de un archivo de ayuda que se asociará con el cuadro de diálogo Dirección. El miembro **lpszHelpFileName** se usa junto con **ulHelpContext** para llamar a la función **WinHelp** de Windows. 
    
**lpfnABSDI**
  
> Puntero a una función MAPI en función del prototipo [ACCELERATEABSDI](accelerateabsdi.md) o null. Este miembro se aplica únicamente a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer. Los clientes que crean una estructura **ADRPARM** para pasar a [IAddrBook:: Address](iaddrbook-address.md) siempre deben establecer el miembro **lpfnABSDI** en NULL. Si se establece la marca DIALOG_SDI, MAPI la establecerá en una función válida antes de volver. Los clientes llaman a esta función desde el bucle de mensajes para asegurarse de que funcionan los aceleradores en el cuadro de diálogo libreta de direcciones. Cuando se descarta el cuadro de diálogo y MAPI llama a la función a la que señala el miembro **lpfnDismiss** , los clientes deben desenlazar la función **ACCELERATEABSDI** del bucle de mensajes. 
    
**lpfnDismiss**
  
> Puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o null. Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo Dirección no modal, para informar a un cliente que llame a **IAddrBook:: Address** , que el cuadro de diálogo ya no está activo. 
    
**lpvDismissContext**
  
> Puntero a la información de contexto que se va a pasar a la función **DISMISSMODELESS** a la que señala el miembro **lpfnDismiss** . Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer. 
    
**lpszCaption**
  
> Puntero al texto que se utilizará como título para el cuadro de diálogo Dirección común.
    
**lpszNewEntryTitle**
  
> Puntero al texto que se va a usar como etiqueta de botón del botón que invoca el cuadro de diálogo **nueva entrada** u otro cuadro de diálogo. 
    
**lpszDestWellsTitle**
  
> Puntero al texto que se va a usar como título de los controles del cuadro de texto del destinatario que pueden aparecer en la versión modal del cuadro de diálogo Dirección común. Este miembro no se usa para los cuadros de diálogo no modales. 
    
**cDestFields**
  
> Número de controles de cuadro de texto de destinatarios en la versión modal del cuadro de diálogo Dirección, o cero si el cuadro de diálogo no tiene modo. El cuadro de diálogo Dirección está abierto para examinar solo cuando se cumplen las siguientes condiciones: 
    
  - El miembro **cDestFields** se establece en cero. 
    
  - Se establece la marca DIALOG_BOX.
    
  - No se ha establecido la marca ADDRESS_ONE.
    
  La configuración de **cDestFields** en 0xFFFFFFFF implica que MAPI debe crear el número predeterminado de controles de cuadro de texto de destinatarios. En este caso, los miembros **lppszDestTitles** y **LPULDESTCOMPS** deben ser nulos. 
    
**nDestFieldFocus**
  
> Indica el control de cuadro de texto en particular que debe tener el foco inicial cuando aparece la versión modal del cuadro de diálogo. Este valor debe estar comprendido entre 0 y el valor de **cDestFields** menos 1. 
    
**lppszDestTitles**
  
> Puntero a una matriz de etiquetas para botones asociados a cada uno de los controles de cuadro de texto que se muestran en la versión modal del cuadro de diálogo Dirección. El valor del miembro **cDestFields** indica el número de etiquetas incluidas en la matriz. Si el miembro **lppszDestTitles** es null, el método de **Dirección** usa los títulos predeterminados. 
    
**lpulDestComps**
  
> Puntero a una matriz de valores de tipo de destinatario, como MAPI_TO, MAPI_CC y MAPI_BCC, que está asociado a cada control de cuadro de texto. El valor del miembro **CDestFields** indica el número de tipos de destinatarios incluidos en la matriz. Los valores a los que apunta **lpulDestComps** se pueden usar para establecer la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatario. Si el miembro **lpulDestComps** es null, el método de **Dirección** usa tipos de destinatarios predeterminados. 
    
**lpContRestriction**
  
> Puntero a una estructura [SRestriction](srestriction.md) que limita el tipo de entradas de dirección que se pueden mostrar en el cuadro de diálogo. 
    
**lpHierRestriction**
  
> Puntero a una estructura **SRestriction** que limita los contenedores de la libreta de direcciones que pueden suministrar entradas de direcciones para que se muestren en el cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los clientes y los proveedores de servicios usan las estructuras **ADRPARM** para controlar la apariencia y el comportamiento de los cuadros de diálogo de direcciones comunes de MAPI. Hay dos variedades del cuadro de diálogo Dirección: sin modo y modal. Algunos de los miembros de la estructura **ADRPARM** se aplican a ambas versiones del cuadro de diálogo, pero algunos solo se aplican a una de las dos versiones. La siguiente tabla relaciona los miembros de una estructura **ADRPARM** con su uso con los cuadros de diálogo de dirección comunes. 
  
|Miembro ADRPARM|Tipo de cuadro de diálogo|
|:-----|:-----|
|**cbABContEntryID** y **lpABContEntryID** <br/> |Modales y no modales  <br/> |
|**ulFlags** <br/> |Modales y no modales  <br/> |
|**lpReserved** <br/> |Modales y no modales  <br/> |
|**ulHelpContext** y **lpszHelpFileName** <br/> |Modales y no modales  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss** y **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |Modales y no modales  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**y **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modales y no modales  <br/> |
|**lpHierRestriction** <br/> |Modales y no modales  <br/> |
   
El cuadro de diálogo no modal es una presentación de solo lectura de las entradas de uno o varios contenedores de libretas de direcciones. El cuadro de diálogo puede mostrar todas las entradas de los contenedores seleccionados o limitarse únicamente a las entradas y contenedores que coinciden con los criterios establecidos por una restricción. La restricción de contenido a la que apunta **lpContRestriction** puede limitar los tipos de entradas que se muestran y la restricción de jerarquía apuntada por **lpHierRestriction** puede limitar los contenedores que proporcionan las entradas. Para informar al autor de la llamada cuando se descarta el cuadro de diálogo, MAPI invoca una función proporcionada por el autor de la llamada que coincide con el prototipo [DISMISSMODELESS](dismissmodeless.md) . Otra función, que coincide con el prototipo [ACCELERATEABSDI](accelerateabsdi.md) , es proporcionada por MAPI e invocada por el autor de la llamada en el bucle de mensajes de Windows para facilitar el trabajo de los métodos abreviados de teclado. La versión no modal del cuadro de diálogo Dirección MAPI se puede mostrar cuando los clientes llaman a [IAddrBook:: Address](iaddrbook-address.md) o cuando los proveedores de servicios llaman a [IMAPISupport:: Address](imapisupport-address.md). 
  
El cuadro de diálogo modal es una presentación de lectura y escritura de entradas de uno o más contenedores. Su contenido puede verse afectado de la misma manera que la versión no modal según las restricciones establecidas en los miembros **lpContRestriction** y **lpHierRestriction** . Además del cuadro de lista que muestra las entradas de contenedor, el cuadro de diálogo modal puede contener entre uno y tres controles de cuadro de texto para conservar entradas seleccionadas por el usuario. Cada control de edición está asociado a un tipo de destinatario concreto o a una propiedad **PR_RECIPIENT_TYPE** , como MAPI_TO. El cuadro de diálogo Dirección modal se puede mostrar mediante cualquiera de los métodos de **Dirección** o cuando los clientes llaman a [IAddrBook::D etails](iaddrbook-details.md) y proveedores de servicios llaman a [IMAPISupport::D etails](imapisupport-details.md). 
  
Esta ilustración incluye dos controles de cuadro de texto porque el miembro **cDestFields** de la estructura **ADRPARM** que controla la visualización de este cuadro de diálogo se establece en 2. El primer control tiene el foco inicial porque el miembro **nDestFieldFocus** está establecido en 0. 
  
El miembro **lpszNewEntryTitle** apunta al texto de una etiqueta de botón que, cuando se selecciona, hace que se muestre un cuadro de diálogo adicional. Normalmente, como se muestra en la ilustración del cuadro de diálogo modal, el botón tiene la etiqueta **New** y el cuadro de diálogo que aparece enumera todos los tipos de direcciones que puede crear cualquiera de los proveedores de la libreta de direcciones en el perfil. Los clientes hacen que se muestre el cuadro de diálogo **nueva entrada** llamando a [IAddrBook:: NEWENTRY](iaddrbook-newentry.md) y pasando cero para el parámetro _cbEidNewEntryTpl_ y null para el parámetro _lpEidNewEntryTpl_ cuando el usuario selecciona el botón. La información que se incluye en este cuadro de diálogo procede de la tabla única de MAPI. 
  
Todas las entradas de este cuadro de diálogo están asociadas a una plantilla para escribir los datos necesarios para crear una dirección del tipo determinado. La mayoría de los proveedores de libreta de direcciones proporcionan una plantilla para cada tipo de entrada de dirección que pueden crear. Cuando un usuario realiza una selección en este cuadro de diálogo, MAPI muestra la plantilla correspondiente.
  
Los cuatro bits más significativos del miembro **ulFlags** de la estructura **ADRPARM** contienen un número de versión que identifica la versión de la estructura **ADRPARM** . La versión actual es 0 (cero) o ADRPARM_HELP_CTX. Se producirá un error en la implementación actual de MAPI para cualquier versión de la estructura distinta de cero. 
  
Las versiones futuras de la estructura pueden ser completamente diferentes; puede que no admitan la estructura version-Zero. Se proporcionan las siguientes macros para extraer el número de versión del miembro **ulFlags** y para combinarlo con los indicadores definidos: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Ver también

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

