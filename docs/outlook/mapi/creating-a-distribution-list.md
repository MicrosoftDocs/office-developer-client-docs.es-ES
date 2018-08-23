---
title: Creación de una lista de distribución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f0a6b7af196073d52ce98037b443569dcd1f41e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582549"
---
# <a name="creating-a-distribution-list"></a>Creación de una lista de distribución

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes pueden crear una lista de distribución directamente en un contenedor modificable como la libreta de direcciones personales (PAB).
  
**Para crear una lista de distribución en la Libreta personal de direcciones**
  
1. Cree una matriz de etiqueta de la propiedad tamaño con la etiqueta de una propiedad, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), como se indica a continuación:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Llame a [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la Libreta personal de direcciones. Si se ha producido un error o **GetPAB** devuelve cero o NULL, no continúe. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir el archivo PAB. El parámetro de salida _ulObjType_ debe establecerse en MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de PAB para recuperar la propiedad PR_DEF_CREATE_DL, la plantilla que se utiliza para crear una lista de distribución. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Si se produce un error de **GetProps** : 
    
   1. Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de la Libreta personal de direcciones para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable** . 
      
   2. Crear una restricción de propiedad para buscar la fila con la columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL." 
      
   3. Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar esta fila. 
    
6. Guarde el identificador de entrada devuelto por **GetProps** o **FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Llamar al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de la Libreta personal de direcciones para crear una nueva entrada con la plantilla representada por el identificador de entrada guardada. No asuma que el objeto devuelto será una lista de distribución en lugar de un usuario de mensajería cuando esta llamada es remota. Tenga en cuenta que el indicador CREATE_CHECK_DUP se pasa en el parámetro _ulFlags_ para impedir que se va a agregar dos veces la entrada. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Llamar al método **IUnknown:: QueryInterface** de la nueva entrada, pasando IID_IDistList como el identificador de interfaz, para determinar si la entrada es una lista de distribución y admite la [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaz. Debido a que **CreateEntry** devuelve un puntero **IMAPIProp** en lugar del puntero **IMailUser** o **IDistList** más específico, compruebe que se ha creado un objeto de lista de distribución. Si **QueryInterface** se realiza correctamente, puede estar seguro de que ha creado una lista de distribución en lugar de un usuario de mensajería. 
    
9. Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la lista de distribución para establecer su nombre para mostrar y otras propiedades. 
    
10. Llamar al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de la lista de distribución para agregar uno o varios usuarios de mensajería. 
    
11. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la lista de distribución cuando esté listo para guardarlo. Para recuperar el identificador de entrada de la lista de distribución guardadas, establecer la marca KEEP_OPEN_READWRITE y, a continuación, llamar a [IMAPIProp::GetProps](imapiprop-getprops.md) que solicita la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. La versión de la nueva lista de distribución y el archivo PAB llamando a sus métodos **IUnknown:: Release** . 
    
13. Llamar a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria para el identificador de entrada de la Libreta personal de direcciones y la matriz de etiqueta tamaño (propiedad). 
    

