---
title: Crear una lista de distribución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7108ae215562169244100a56cc9b9208d78b1893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424178"
---
# <a name="creating-a-distribution-list"></a>Crear una lista de distribución

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes pueden crear una lista de distribución directamente en un contenedor modificable, como la libreta de direcciones personal (PAB).
  
**Para crear una lista de distribución en el PAB**
  
1. Cree una matriz de etiquetas de propiedad de tamaño con una etiqueta de **propiedad, PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), de la siguiente manera:
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Llame [a IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada del PAB. Si hay un error o **GetPAB** devuelve cero o NULL, no continúe. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Llame [a IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir el PAB. El  _parámetro de salida ulObjType_ debe establecerse en MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del PAB para recuperar la propiedad PR_DEF_CREATE_DL, la plantilla que usa para crear una lista de distribución. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Si **se produce un error en GetProps:** 
    
   1. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del PAB para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable.** 
      
   2. Cree una restricción de propiedad para buscar la fila con la **columna PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL". 
      
   3. Llame [a IMAPITable::FindRow](imapitable-findrow.md) para localizar esta fila. 
    
6. Guarde el identificador de entrada devuelto por **GetProps** o **FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) del PAB para crear una nueva entrada con la plantilla representada por el identificador de entrada guardado. No suponga que el objeto devuelto será una lista de distribución en lugar de un usuario de mensajería cuando esta llamada esté remota. Observe que la CREATE_CHECK_DUP se pasa en el  _parámetro ulFlags_ para evitar que la entrada se pueda agregar dos veces. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Llama al método **IUnknown::QueryInterface** de la nueva entrada, pasando IID_IDistList como identificador de interfaz, para determinar si la entrada es una lista de distribución y admite la interfaz [IDistList : IMAPIContainer.](idistlistimapicontainer.md) Dado **que CreateEntry** devuelve un puntero **IMAPIProp** en lugar del puntero **IMailUser** o **IDistList** más específico, compruebe que se haya creado un objeto de lista de distribución. Si **QueryInterface se** realiza correctamente, puede estar seguro de que ha creado una lista de distribución en lugar de un usuario de mensajería. 
    
9. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la lista de distribución para establecer su nombre para mostrar y otras propiedades. 
    
10. Llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de la lista de distribución para agregar uno o más usuarios de mensajería. 
    
11. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la lista de distribución cuando esté listo para guardarlo. Para recuperar el identificador de entrada de la lista de distribución guardada, establezca la marca KEEP_OPEN_READWRITE y, a continuación, llame a [IMAPIProp::GetProps](imapiprop-getprops.md) solicitando la **propiedad PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. Libera la nueva lista de distribución y pab mediante una llamada a sus métodos **IUnknown::Release.** 
    
13. Llama [a MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria del identificador de entrada del PAB y la matriz de etiquetas de propiedad de tamaño. 
    

