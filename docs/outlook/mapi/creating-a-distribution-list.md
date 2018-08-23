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
# <a name="creating-a-distribution-list"></a><span data-ttu-id="c3821-103">Creación de una lista de distribución</span><span class="sxs-lookup"><span data-stu-id="c3821-103">Creating a distribution list</span></span>

<span data-ttu-id="c3821-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3821-105">Los clientes pueden crear una lista de distribución directamente en un contenedor modificable como la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="c3821-105">Clients can create a distribution list directly into a modifiable container such as the personal address book (PAB).</span></span>
  
<span data-ttu-id="c3821-106">**Para crear una lista de distribución en la Libreta personal de direcciones**</span><span class="sxs-lookup"><span data-stu-id="c3821-106">**To create a distribution list in the PAB**</span></span>
  
1. <span data-ttu-id="c3821-107">Cree una matriz de etiqueta de la propiedad tamaño con la etiqueta de una propiedad, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="c3821-107">Create a sized property tag array with one property tag, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), as follows:</span></span>
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. <span data-ttu-id="c3821-108">Llame a [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la Libreta personal de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c3821-108">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> <span data-ttu-id="c3821-109">Si se ha producido un error o **GetPAB** devuelve cero o NULL, no continúe.</span><span class="sxs-lookup"><span data-stu-id="c3821-109">If there is an error or **GetPAB** returns zero or NULL, do not continue.</span></span> 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. <span data-ttu-id="c3821-110">Llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir el archivo PAB.</span><span class="sxs-lookup"><span data-stu-id="c3821-110">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the PAB.</span></span> <span data-ttu-id="c3821-111">El parámetro de salida _ulObjType_ debe establecerse en MAPI_ABCONT.</span><span class="sxs-lookup"><span data-stu-id="c3821-111">The  _ulObjType_ output parameter should be set to MAPI_ABCONT.</span></span> 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. <span data-ttu-id="c3821-112">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de PAB para recuperar la propiedad PR_DEF_CREATE_DL, la plantilla que se utiliza para crear una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c3821-112">Call the PAB's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the PR_DEF_CREATE_DL property, the template that it uses to create a distribution list.</span></span> 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. <span data-ttu-id="c3821-113">Si se produce un error de **GetProps** :</span><span class="sxs-lookup"><span data-stu-id="c3821-113">If **GetProps** fails:</span></span> 
    
   1. <span data-ttu-id="c3821-114">Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de la Libreta personal de direcciones para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) con la interfaz **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="c3821-114">Call the PAB's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> 
      
   2. <span data-ttu-id="c3821-115">Crear una restricción de propiedad para buscar la fila con la columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) igual a "MAPIPDL."</span><span class="sxs-lookup"><span data-stu-id="c3821-115">Create a property restriction to search for the row with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column equal to "MAPIPDL."</span></span> 
      
   3. <span data-ttu-id="c3821-116">Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar esta fila.</span><span class="sxs-lookup"><span data-stu-id="c3821-116">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate this row.</span></span> 
    
6. <span data-ttu-id="c3821-117">Guarde el identificador de entrada devuelto por **GetProps** o **FindRow**.</span><span class="sxs-lookup"><span data-stu-id="c3821-117">Save the entry identifier returned by either **GetProps** or **FindRow**.</span></span>
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. <span data-ttu-id="c3821-118">Llamar al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de la Libreta personal de direcciones para crear una nueva entrada con la plantilla representada por el identificador de entrada guardada.</span><span class="sxs-lookup"><span data-stu-id="c3821-118">Call the PAB's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new entry using the template represented by the saved entry identifier.</span></span> <span data-ttu-id="c3821-119">No asuma que el objeto devuelto será una lista de distribución en lugar de un usuario de mensajería cuando esta llamada es remota.</span><span class="sxs-lookup"><span data-stu-id="c3821-119">Do not assume that the object returned will be a distribution list rather than a messaging user when this call is remoted.</span></span> <span data-ttu-id="c3821-120">Tenga en cuenta que el indicador CREATE_CHECK_DUP se pasa en el parámetro _ulFlags_ para impedir que se va a agregar dos veces la entrada.</span><span class="sxs-lookup"><span data-stu-id="c3821-120">Notice that the CREATE_CHECK_DUP flag is passed in the  _ulFlags_ parameter to prevent the entry from being added twice.</span></span> 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. <span data-ttu-id="c3821-121">Llamar al método **IUnknown:: QueryInterface** de la nueva entrada, pasando IID_IDistList como el identificador de interfaz, para determinar si la entrada es una lista de distribución y admite la [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="c3821-121">Call the new entry's **IUnknown::QueryInterface** method, passing IID_IDistList as the interface identifier, to determine if the entry is a distribution list and supports the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span> <span data-ttu-id="c3821-122">Debido a que **CreateEntry** devuelve un puntero **IMAPIProp** en lugar del puntero **IMailUser** o **IDistList** más específico, compruebe que se ha creado un objeto de lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c3821-122">Because **CreateEntry** returns an **IMAPIProp** pointer rather than the more specific **IMailUser** or **IDistList** pointer, check that a distribution list object was created.</span></span> <span data-ttu-id="c3821-123">Si **QueryInterface** se realiza correctamente, puede estar seguro de que ha creado una lista de distribución en lugar de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c3821-123">If **QueryInterface** succeeds, you can be sure that you have created a distribution list rather than a messaging user.</span></span> 
    
9. <span data-ttu-id="c3821-124">Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la lista de distribución para establecer su nombre para mostrar y otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="c3821-124">Call the distribution list's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set its display name and other properties.</span></span> 
    
10. <span data-ttu-id="c3821-125">Llamar al método [IABContainer::CreateEntry](iabcontainer-createentry.md) de la lista de distribución para agregar uno o varios usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c3821-125">Call the distribution list's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to add one or more messaging users.</span></span> 
    
11. <span data-ttu-id="c3821-126">Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la lista de distribución cuando esté listo para guardarlo.</span><span class="sxs-lookup"><span data-stu-id="c3821-126">Call the distribution list's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when you're ready to save it.</span></span> <span data-ttu-id="c3821-127">Para recuperar el identificador de entrada de la lista de distribución guardadas, establecer la marca KEEP_OPEN_READWRITE y, a continuación, llamar a [IMAPIProp::GetProps](imapiprop-getprops.md) que solicita la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c3821-127">To retrieve the entry identifier of the saved distribution list, set the KEEP_OPEN_READWRITE flag and then call [IMAPIProp::GetProps](imapiprop-getprops.md) requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
12. <span data-ttu-id="c3821-128">La versión de la nueva lista de distribución y el archivo PAB llamando a sus métodos **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="c3821-128">Release the new distribution list and the PAB by calling their **IUnknown::Release** methods.</span></span> 
    
13. <span data-ttu-id="c3821-129">Llamar a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria para el identificador de entrada de la Libreta personal de direcciones y la matriz de etiqueta tamaño (propiedad).</span><span class="sxs-lookup"><span data-stu-id="c3821-129">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the memory for the entry identifier of the PAB and the sized property tag array.</span></span> 
    

