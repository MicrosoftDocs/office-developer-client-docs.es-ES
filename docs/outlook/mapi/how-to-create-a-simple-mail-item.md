---
title: Crear un elemento de correo simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1bbf80c8f614fc5e69773407c7882f3df8c0c81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816963"
---
# <a name="create-a-simple-mail-item"></a>Crear un elemento de correo simple
  
**Hace referencia a**: Outlook 
  
MAPI se puede usar para crear y enviar un mensaje que solicita una confirmación de lectura. Cuando se solicita una confirmación de lectura, el sistema de mensajería genera y devuelve un informe de lectura al remitente cuando el destinatario abre el mensaje.
  
Para obtener información acerca de cómo descargar, ver y ejecutar el código de la aplicación MFCMAPI y el proyecto de CreateOutlookItemsAddin hace referencia en este tema, vea [instalar los ejemplos que se usa en esta sección](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Para crear y enviar un mensaje que solicita una confirmación de lectura

1. Crear un mensaje saliente. Para obtener información acerca de cómo crear un mensaje saliente, vea [control de un mensaje saliente](handling-an-outgoing-message.md).
    
2. Agregue la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y se establece en **true**.
    
3. Agregue la propiedad **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Agregue la propiedad **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Enviar el mensaje al llamar al método [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
El `AddMail` (función) en el archivo de origen Mails.cpp del proyecto CreateOutlookItemsAddin muestra estos pasos. El `AddMail` función toma parámetros desde el cuadro de diálogo **Agregar correo** que se muestra al hacer clic en el comando **Agregar correo** en el menú **Addins** en la aplicación de ejemplo MFCMAPI. El `DisplayAddMailDialog` función en Mails.cpp muestra el cuadro de diálogo y pasa los valores desde el cuadro de diálogo para el `AddMail` (función). El `DisplayAddMailDialog` función no directamente relacionados con la creación de un elemento de correo con MAPI, por lo que no se incluye aquí. El `AddMail` (función) se enumeran a continuación. 
  
Tenga en cuenta que el parámetro _lpFolder_ se pasa a la `AddMail` método es un puntero a una interfaz [IMAPIFolder](imapifolderimapicontainer.md) que representa la carpeta donde se creará el nuevo mensaje. Dado que el parámetro _lpFolder_ que representa una interfaz **IMAPIFolder** , el código llama al método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . El método **CreateMessage** devuelve un código de éxito y un puntero a un puntero a un [IMessage: IMAPIProp](imessageimapiprop.md) interfaz. 

La mayoría de los `AddMail` código de función controla el trabajo de configuración de propiedades en la preparación para llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) . Si la llamada al método **SetProps** se realiza correctamente, una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) confirma los cambios en el almacén y crea un nuevo elemento de correo. A continuación, si se solicita, se llama al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje. 
  
El `AddMail` función utiliza dos funciones auxiliares para generar valores para las propiedades **PR_CONVERSATION_INDEX** y **PR_REPORT_TAG** : el `BuildConversationIndex` y `AddReportTag` funciones. El `BuildConversationIndex` función, que se encuentra en CreateOutlookItemsAddin.cpp, realiza el mismo trabajo que la función integrada de MAPI [ScCreateConversationIndex](sccreateconversationindex.md) hace cuando un índice de conversación primario no se pasa a ella. El formato del búfer de índice de conversación que generan estas funciones se documenta en [Propiedad canónico PidTagConversationIndex](pidtagconversationindex-canonical-property.md). 

El `AddReportTag` a su vez llama la función, que se encuentra en Mails.cpp, el `BuildReportTag` (función) para crear una estructura de la propiedad **PR_REPORT_TAG** . Para obtener información acerca de la estructura que el `BuildReportTag` compilaciones de función, vea [La propiedad canónico PidTagReportTag](pidtagreporttag-canonical-property.md).
  
La siguiente es una lista completa de la `AddMail` (función). 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a>Vea también

- [Uso de MAPI para crear elementos de Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

