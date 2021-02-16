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
# <a name="creating-a-distribution-list"></a><span data-ttu-id="b264c-103">Crear una lista de distribución</span><span class="sxs-lookup"><span data-stu-id="b264c-103">Creating a distribution list</span></span>

<span data-ttu-id="b264c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b264c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b264c-105">Los clientes pueden crear una lista de distribución directamente en un contenedor modificable, como la libreta de direcciones personal (PAB).</span><span class="sxs-lookup"><span data-stu-id="b264c-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="b264c-106">**Para crear una lista de distribución en el PAB**</span><span class="sxs-lookup"><span data-stu-id="b264c-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="b264c-107">Cree una matriz de etiquetas de propiedad de tamaño con una etiqueta de **propiedad, PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b264c-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="b264c-108">Llame [a IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada del PAB.</span><span class="sxs-lookup"><span data-stu-id="b264c-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="b264c-109">Si hay un error o **GetPAB** devuelve cero o NULL, no continúe.</span><span class="sxs-lookup"><span data-stu-id="b264c-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="b264c-110">Llame [a IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir el PAB.</span><span class="sxs-lookup"><span data-stu-id="b264c-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="b264c-111">El  _parámetro de salida ulObjType_ debe establecerse en MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="b264c-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="b264c-112">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del PAB para recuperar la propiedad PR_DEF_CREATE_DL, la plantilla que usa para crear una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b264c-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="b264c-113">Si **se produce un error en GetProps:**</span><span class="sxs-lookup"><span data-stu-id="b264c-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="b264c-114">Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del PAB para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="b264c-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="b264c-115">Cree una restricción de propiedad para buscar la fila con la **columna PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL".</span><span class="sxs-lookup"><span data-stu-id="b264c-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="b264c-116">Llame [a IMAPITable::FindRow](imapitable-findrow.md) para localizar esta fila.</span><span class="sxs-lookup"><span data-stu-id="b264c-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="b264c-117">Guarde el identificador de entrada devuelto por **GetProps** o **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="b264c-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="b264c-118">Llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) del PAB para crear una nueva entrada con la plantilla representada por el identificador de entrada guardado.</span><span class="sxs-lookup"><span data-stu-id="b264c-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="b264c-119">No suponga que el objeto devuelto será una lista de distribución en lugar de un usuario de mensajería cuando esta llamada esté remota.</span><span class="sxs-lookup"><span data-stu-id="b264c-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="b264c-120">Observe que la CREATE_CHECK_DUP se pasa en el  _parámetro ulFlags_ para evitar que la entrada se pueda agregar dos veces.</span><span class="sxs-lookup"><span data-stu-id="b264c-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="b264c-121">Llama al método **IUnknown::QueryInterface** de la nueva entrada, pasando IID_IDistList como identificador de interfaz, para determinar si la entrada es una lista de distribución y admite la interfaz [IDistList : IMAPIContainer.](idistlistimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="b264c-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="b264c-122">Dado **que CreateEntry** devuelve un puntero **IMAPIProp** en lugar del puntero **IMailUser** o **IDistList** más específico, compruebe que se haya creado un objeto de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b264c-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="b264c-123">Si **QueryInterface se** realiza correctamente, puede estar seguro de que ha creado una lista de distribución en lugar de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b264c-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="b264c-124">Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la lista de distribución para establecer su nombre para mostrar y otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="b264c-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="b264c-125">Llama al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de la lista de distribución para agregar uno o más usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b264c-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="b264c-126">Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la lista de distribución cuando esté listo para guardarlo.</span><span class="sxs-lookup"><span data-stu-id="b264c-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="b264c-127">Para recuperar el identificador de entrada de la lista de distribución guardada, establezca la marca KEEP_OPEN_READWRITE y, a continuación, llame a [IMAPIProp::GetProps](imapiprop-getprops.md) solicitando la **propiedad PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b264c-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="b264c-128">Libera la nueva lista de distribución y pab mediante una llamada a sus métodos **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="b264c-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="b264c-129">Llama [a MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria del identificador de entrada del PAB y la matriz de etiquetas de propiedad de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b264c-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

