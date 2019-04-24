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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333029"
---
# <a name="creating-a-distribution-list"></a><span data-ttu-id="013b3-103">Crear una lista de distribución</span><span class="sxs-lookup"><span data-stu-id="013b3-103">Creating a distribution list</span></span>

<span data-ttu-id="013b3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="013b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="013b3-105">Los clientes pueden crear una lista de distribución directamente en un contenedor modificable como la libreta personal de direcciones (PAB).</span><span class="sxs-lookup"><span data-stu-id="013b3-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="013b3-106">**Para crear una lista de distribución en la PAB**</span><span class="sxs-lookup"><span data-stu-id="013b3-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="013b3-107">Cree una matriz de etiquetas de propiedad con tamaño con una etiqueta de propiedad, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="013b3-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="013b3-108">Llame a [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la PAB.</span><span class="sxs-lookup"><span data-stu-id="013b3-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="013b3-109">Si hay un error o **GetPAB** devuelve cero o null, no continúe.</span><span class="sxs-lookup"><span data-stu-id="013b3-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="013b3-110">Llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) para abrir la PAB.</span><span class="sxs-lookup"><span data-stu-id="013b3-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="013b3-111">El parámetro de salida _ulObjType_ debe establecerse en MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="013b3-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="013b3-112">Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del PAB para recuperar la propiedad PR_DEF_CREATE_DL, la plantilla que utiliza para crear una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="013b3-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="013b3-113">Si **GetProps** produce un error:</span><span class="sxs-lookup"><span data-stu-id="013b3-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="013b3-114">Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de PAB para abrir la **propiedad PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="013b3-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="013b3-115">Cree una restricción de propiedad para buscar la fila con la columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL".</span><span class="sxs-lookup"><span data-stu-id="013b3-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="013b3-116">Llame al [IMAPITable:: FindRow](imapitable-findrow.md) para localizar esta fila.</span><span class="sxs-lookup"><span data-stu-id="013b3-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="013b3-117">Guarde el identificador de entrada devuelto por **GetProps** o **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="013b3-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="013b3-118">Llame al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) de PAB para crear una nueva entrada mediante la plantilla representada por el identificador de entrada guardada.</span><span class="sxs-lookup"><span data-stu-id="013b3-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="013b3-119">No suponga que el objeto devuelto será una lista de distribución en lugar de un usuario de mensajería cuando esta llamada se realice de forma remota.</span><span class="sxs-lookup"><span data-stu-id="013b3-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="013b3-120">Observe que la marca CREATE_CHECK_DUP se pasa en el parámetro _ulFlags_ para evitar que la entrada se agregue dos veces.</span><span class="sxs-lookup"><span data-stu-id="013b3-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="013b3-121">Llame al método **IUnknown:: QueryInterface** del nuevo elemento, pasando IID_IDistList como identificador de interfaz, para determinar si la entrada es una lista de distribución y es compatible con la interfaz [IDistList: IMAPIContainer](idistlistimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="013b3-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="013b3-122">Como **CreateEntry** devuelve un puntero **IMAPIProp** en lugar del puntero de **IMailUser** o **IDistList** más específicos, compruebe que se haya creado un objeto de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="013b3-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="013b3-123">Si **QueryInterface** se ejecuta correctamente, puede asegurarse de que ha creado una lista de distribución en lugar de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="013b3-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="013b3-124">Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) de la lista de distribución para establecer su nombre para mostrar y otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="013b3-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="013b3-125">Llame al método [IABContainer:: CreateEntry](iabcontainer-createentry.md) de la lista de distribución para agregar uno o más usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="013b3-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="013b3-126">Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la lista de distribución cuando esté listo para guardarlo.</span><span class="sxs-lookup"><span data-stu-id="013b3-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="013b3-127">Para recuperar el identificador de entrada de la lista de distribución guardada, establezca la marca KEEP_OPEN_READWRITE y, a continuación, llame a [IMAPIProp:: GetProps](imapiprop-getprops.md) solicitando la propiedad del valor ([PidTagEntryId](pidtagentryid-canonical-property.md)). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="013b3-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="013b3-128">Para liberar la nueva lista de distribución y la PAB, llame a sus métodos **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="013b3-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="013b3-129">Llame a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria del identificador de entrada de la PAB y la matriz de etiquetas de propiedad con tamaño.</span><span class="sxs-lookup"><span data-stu-id="013b3-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

