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
ms.openlocfilehash: 560cae5e8a3d73d80a4907fd0fec43b389ef9fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572028"
---
# <a name="adrparm"></a>ADRPARM

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la presentación y el comportamiento del cuadro de diálogo dirección comunes. 
  
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

## <a name="members"></a>Members

**cbABContEntryID**
  
> Recuento de bytes en el identificador de entrada que señala **lpABContEntryID**.
    
**lpABContEntryID**
  
> Puntero al identificador de entrada del contenedor que proporciona la lista de direcciones de destinatarios que se muestran en el cuadro de diálogo dirección inicial.
    
**ulFlags**
  
> Máscara de bits de indicadores asociados con varias opciones del cuadro de diálogo dirección. Se pueden establecer los siguientes indicadores:
    
AB_RESOLVE
  
> Habilitar todos los nombres de resolverse después de cerrar el cuadro de diálogo dirección. Si hay entradas ambiguas derivados del proceso de resolución de nombres, aparece un cuadro de diálogo preguntar al usuario para obtener ayuda en la resolución de ellos. Configuración de esta marca garantiza que todos los nombres devueltos por [IAddrBook::Address](iaddrbook-address.md) se resuelven. 
    
AB_SELECTONLY
  
> Deshabilitar la creación de direcciones de uso único para una lista de destinatarios. Esta marca sólo se utiliza si el cuadro de diálogo es modal, indicada por el indicador DIALOG_MODAL que se va a establecer.
    
ADDRESS_ONE
  
> El usuario puede seleccionar a exactamente un destinatario en lugar de varios destinatarios de una lista. Esta marca sólo es válida cuando **cDestFields** es cero y el cuadro de diálogo es modal, indicada por el indicador DIALOG_MODAL que se va a establecer. 
    
DIALOG_MODAL
  
> Hace que la versión modal del cuadro de diálogo dirección comunes que se mostrará. Se debe establecer este indicador o DIALOG_SDI; no ambos pueden establecerse. 
    
DIALOG_OPTIONS
  
> Hace que el botón **Opciones de envío** que se mostrará en el cuadro de diálogo. Esta marca sólo se utiliza si el cuadro de diálogo es modal, indicada por el indicador DIALOG_MODAL que se va a establecer. 
    
DIALOG_SDI
  
> Hace que la versión no modal del cuadro de diálogo dirección comunes que se mostrará. Se debe establecer este indicador o DIALOG_MODAL; no ambos pueden establecerse. El indicador DIALOG_SDI se omite para los clientes de Outlook no, y se mostrará la versión del cuadro de diálogo modal. Por consiguiente, no se debe esperar un puntero a un identificador en el parámetro _lpulUIParam_ de [IAddrBook::Address](iaddrbook-address.md).
    
**lpReserved**
  
> Reservado, debe ser cero.
    
**ulHelpContext**
  
> Especifica el contexto de **Ayuda** que primero se mostrará cuando el usuario hace clic en el botón Ayuda en el cuadro de diálogo dirección. 
    
**lpszHelpFileName**
  
> Puntero en el nombre de un archivo de ayuda que se asociará con el cuadro de diálogo dirección. El miembro **lpszHelpFileName** se usa junto con **ulHelpContext** para llamar a la función de **Ayuda** de Windows. 
    
**lpfnABSDI**
  
> Puntero a una función MAPI basándose en el prototipo [ACCELERATEABSDI](accelerateabsdi.md) o NULL. Este miembro se aplica a la versión de solo, el cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer. Los clientes de creación de una estructura **ADRPARM** que se pase a [IAddrBook::Address](iaddrbook-address.md) siempre deben establecer al miembro **lpfnABSDI** en NULL. Si se establece la marca DIALOG_SDI, MAPI, a continuación, establecerá a una función válida antes de devolverlo. Los clientes de llaman a esta función desde en su bucle de mensajes para asegurarse de que los aceleradores en la dirección de trabajo del cuadro de diálogo del libro. Cuando se descarta el cuadro de diálogo y MAPI llama a la función indicada por el miembro **lpfnDismiss** , los clientes deben eliminar enlaces de la función **ACCELERATEABSDI** desde su bucle de mensajes. 
    
**lpfnDismiss**
  
> Puntero a una función basándose en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL. Este miembro sólo se aplica a la versión de solo, el cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer. MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente de una llamada a **IAddrBook::Address** que el cuadro de diálogo ya no está activo. 
    
**lpvDismissContext**
  
> Puntero a la información de contexto que se pasan a la función **DISMISSMODELESS** que señala el miembro **lpfnDismiss** . Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer. 
    
**lpszCaption**
  
> Puntero al texto que se usará como el título para el cuadro de diálogo dirección común.
    
**lpszNewEntryTitle**
  
> Puntero al texto que se usará como la etiqueta del botón para el botón que invoca el cuadro de diálogo **Nueva entrada** o en otro cuadro de diálogo. 
    
**lpszDestWellsTitle**
  
> Puntero al texto que se usará como un título para los controles de cuadro de texto de destinatarios que pueden aparecer en la versión modal del cuadro de diálogo dirección comunes. Este miembro no se usa para cuadros de diálogo no modal. 
    
**cDestFields**
  
> Recuento de controles de cuadro de texto de destinatario en la versión modal del cuadro de diálogo dirección, o cero si el cuadro de diálogo es no modal. El cuadro de diálogo dirección está abierto para la exploración sólo cuando se cumplan las condiciones siguientes: 
    
  - El miembro **cDestFields** se establece en cero. 
    
  - Se establece la marca DIALOG_BOX.
    
  - No se establece la marca ADDRESS_ONE.
    
  Si se establece **cDestFields** en 0XFFFFFFFF implica que MAPI debe crear el número predeterminado de destinatario texto controles de cuadro. En este caso, los miembros **lppszDestTitles** y **lpulDestComps** deben ser NULL. 
    
**nDestFieldFocus**
  
> Indica el control de cuadro de texto concreto que debe tener el foco inicial cuando aparece la versión del cuadro de diálogo modal. Este valor debe ser entre 0 y el valor de **cDestFields** menos 1. 
    
**lppszDestTitles**
  
> Puntero a una matriz de las etiquetas de los botones asociados con cada uno de los controles de cuadro de texto que se muestran en la versión la dirección del cuadro de diálogo modal. El valor del miembro **cDestFields** indica el número de etiquetas que se incluyen en la matriz. Si el miembro **lppszDestTitles** es NULL, el método **dirección** utiliza los títulos de forma predeterminada. 
    
**lpulDestComps**
  
> Puntero a una matriz de valores de tipo de destinatario, como MAPI_TO, MAPI_CC y MAPI_BCC, que está asociada con cada control de cuadro de texto. El valor del miembro **CDestFields** indica el número de tipos de destinatarios incluidos en la matriz. Los valores que señala **lpulDestComps** pueden usarse para establecer la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatario. Si el miembro **lpulDestComps** es NULL, el método **dirección** usa tipos de destinatarios de forma predeterminada. 
    
**lpContRestriction**
  
> Puntero a una estructura [SRestriction](srestriction.md) que limita el tipo de las entradas de dirección que se pueden mostrar en el cuadro de diálogo. 
    
**lpHierRestriction**
  
> Puntero a una estructura **SRestriction** que limita los contenedores de la libreta de direcciones que pueden proporcionar las entradas de dirección que se mostrará en el cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

**ADRPARM** estructuras usadas por los clientes y proveedores de servicios para controlar la apariencia y el comportamiento de los cuadros de diálogo de dirección comunes de MAPI. Existen dos variedades dentro del cuadro de diálogo dirección: modal y no modal. Algunos de los miembros de la estructura de **ADRPARM** se aplican a ambas versiones del cuadro de diálogo, pero algunas sólo se aplican a una de las dos versiones. En la tabla siguiente relaciona a los miembros de una estructura **ADRPARM** para su uso con los cuadros de diálogo dirección comunes. 
  
|Miembro ADRPARM|Tipo del cuadro de diálogo|
|:-----|:-----|
|**cbABContEntryID** y **lpABContEntryID** <br/> |Modal y no modal  <br/> |
|**ulFlags** <br/> |Modal y no modal  <br/> |
|**lpReserved** <br/> |Modal y no modal  <br/> |
|**ulHelpContext** y **lpszHelpFileName** <br/> |Modal y no modal  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss** y **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |Modal y no modal  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**y **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal y no modal  <br/> |
|**lpHierRestriction** <br/> |Modal y no modal  <br/> |
   
El cuadro de diálogo no modal es una presentación de sólo lectura de las entradas de uno o varios contenedores de la libreta de direcciones. El cuadro de diálogo puede mostrar todas las entradas de los contenedores seleccionados o estar limitada sólo a esas entradas y contenedores que coinciden con los criterios establecidos por una restricción. La restricción de contenido que señala **lpContRestriction** puede limitar los tipos de entradas que se muestran y la restricción de jerarquía que señala **lpHierRestriction** puede limitar los contenedores que proporciona las entradas. Para informar al autor de la llamada cuando se cierra el cuadro de diálogo, MAPI invoca una función que es proporcionada por el autor de la llamada que coincida con el prototipo [DISMISSMODELESS](dismissmodeless.md) . Otra función, uno que coincida con el prototipo [ACCELERATEABSDI](accelerateabsdi.md) , es proporcionada por MAPI y es invocado por el autor de la llamada en el bucle de mensajes de Windows para facilitar el trabajo de métodos abreviados de teclado. La versión no modal del cuadro de diálogo Dirección MAPI se puede mostrar cuando los clientes llaman [IAddrBook::Address](iaddrbook-address.md) o cuando los proveedores de servicios llama a [IMAPISupport::Address](imapisupport-address.md). 
  
El cuadro de diálogo modal es una presentación de lectura y escritura de las entradas de uno o varios contenedores. Su contenido puede verse afectado de la misma manera como la versión no modal por restricciones del conjunto en el **lpContRestriction** y **lpHierRestriction** (miembros). Además del cuadro de lista mostrar las entradas de contenedor, el cuadro de diálogo modal puede contener entre uno y tres controles de cuadro de texto para contener las entradas seleccionadas por el usuario. Cada control de edición está asociado con un tipo de destinatario concreto o una propiedad **PR_RECIPIENT_TYPE** como MAPI_TO. El cuadro de diálogo modal dirección puede mostrarse por cualquiera de los métodos de **dirección** o cuando los clientes [IAddrBook::Details](iaddrbook-details.md) y proveedores de servicios de llamadas [IMAPISupport::Details](imapisupport-details.md). 
  
Esta ilustración incluye dos controles de cuadro de texto debido a que el miembro **cDestFields** de la estructura **ADRPARM** controlar la presentación de este cuadro de diálogo está establecido a 2. El primer control tiene el foco inicial debido a que el miembro **nDestFieldFocus** se establece en 0. 
  
El miembro **lpszNewEntryTitle** apunta a texto para una etiqueta del botón que, cuando se selecciona, hace que un cuadro de diálogo adicional que se mostrará. Normalmente, tal y como se muestra en la ilustración del cuadro de diálogo modal, el botón tiene la etiqueta **New** y el cuadro de diálogo que aparece, enumera todos los tipos de direcciones que se pueden crear mediante cualquiera de los proveedores de la libreta de direcciones en el perfil. Clientes de hacer este cuadro de diálogo **Nueva entrada** que se mostrará al llamar a [IAddrBook::NewEntry](iaddrbook-newentry.md) y pasando NULL para el parámetro _lpEidNewEntryTpl_ y cero para el parámetro _cbEidNewEntryTpl_ cuando el usuario selecciona el botón. La información que se incluye en este cuadro de diálogo procede de la tabla de uso único de MAPI. 
  
Todas las entradas de este cuadro de diálogo está asociada con una plantilla para escribir los datos necesarios para crear una dirección del tipo determinado. La mayoría de los proveedores de la libreta de direcciones proporcionan una plantilla para cada tipo de entrada de dirección que pueden crear. Cuando un usuario realiza una selección de este cuadro de diálogo, MAPI muestra la plantilla correspondiente.
  
Los bits más significativos de cuatro de miembro de la estructura **ADRPARM** **ulFlags** contienen un número de versión que identifica la versión de la estructura **ADRPARM** . La versión actual es 0 (cero) o ADRPARM_HELP_CTX. Se producirá un error en la implementación actual de MAPI para cualquier versión de la estructura de distinto de cero. 
  
Las futuras versiones de la estructura pueden ser completamente diferentes; es posible que no admiten la estructura de la versión de cero. Para extraer el número de versión desde el miembro **ulFlags** y para combinar con los indicadores definidos, se proporcionan las siguientes macros: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Recursos adicionales

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Estructuras MAPI](mapi-structures.md)

