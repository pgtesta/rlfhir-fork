## {{page-title}}

I parametri di ricerca definiti nel profilo RLOrganizationL1 sono definiti nella seguente tabella:

<table>
  <thead>
    <tr>
      <th width="15%">Nome</th>
      <th width="25%">Descrizione</th>
      <th width="30%">URL</th>
      <th width="30%">Espressione</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>RLOrganizationDataFineValidita</td>
      <td>
        Parametro di ricerca di strutture SISS di livello 1 e livello 2
        specificando la data di fine validità.
      </td>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataFineValidita}}
      </td>
      <td>
        extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataFineValidita').value
      </td>
    </tr>
    <tr>
      <td>RLOrganizationDataInizioValidita</td>
      <td>
        Parametro di ricerca di strutture SISS di livello 1 e livello 2
        specificando la data di inserimento.
      </td>
      <td>
        {{link:https://fhir.siss.regione.lombardia.it/SearchParameter/RLOrganizationDataInizioValidita}}
      </td>
      <td>
        extension.where(url='https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationDataInizioValidita').value
      </td>
    </tr>
  </tbody>
</table>

<br>